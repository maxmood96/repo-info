## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1deb2c28492aefad30d3769541efaf72286f2ad6a663e129cf30ffa0a0ffed37
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

### `eclipse-temurin:17-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:659f37e8f7dba78d0ff248de9eaa600c8b371c79dd9841e0359f2073ef79e298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211914649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55f9b113989bd6b15ff77b7bcabab3bb98c63673af0afc88c20c3990d26f11e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64le)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        x86_64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Mon, 28 Apr 2025 16:55:19 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c4683ffcd7accd1ed24c4d55bf6da40c97f805258a5033a691c53f4613854d`  
		Last Modified: Tue, 29 Apr 2025 16:39:29 GMT  
		Size: 27.6 MB (27553684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5bc6b941d8da2ffc323ed484d4f0fd69647285616b6813b677523596b1dad2`  
		Last Modified: Tue, 29 Apr 2025 16:39:31 GMT  
		Size: 144.6 MB (144643991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcfdd83242573721aac325ba99dbb686e81209e1e7a24a21b57f60e4891bfc1`  
		Last Modified: Tue, 29 Apr 2025 16:39:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e9101e3c522794a228c007512843b6ae83d8cb9e8013198ed76f43727576b4`  
		Last Modified: Tue, 29 Apr 2025 16:39:28 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:624dc5dbc9c30b4f1b77a3a250b32de9bcc8fcad7fb7480ae87e31fa92cd5af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2476618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db2bdd52c8977393e6aee5fc2f5f1883ef808fe55c20b6692b33580e821076e`

```dockerfile
```

-	Layers:
	-	`sha256:d52f6c0e2c1bcec8b79e3fc6e721a423f04085eaf44ad5db72dde371750af0a7`  
		Last Modified: Tue, 29 Apr 2025 16:39:28 GMT  
		Size: 2.5 MB (2455461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1991fea81bab75d7abd9310c60c6119a43981a85a6fd321c8b3902dc05c9596b`  
		Last Modified: Tue, 29 Apr 2025 16:39:28 GMT  
		Size: 21.2 KB (21157 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2b5cbbd8ee2b8c04aea78e0e98b8d51549afebcb2dea6dcd8d118e811cd851dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209397393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50accb4bb6f1f68ba3a10c94282083ad44769ce0f0ebf4a6b36e1cc4874e9a3c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:37e2781211ed66b85e838f75f63c4036aeedc358075b7ac677bbe4ad43998692 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-04-28T15:48:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64le)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        x86_64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:2aa6bd15812764b98217de512ddcd6b7fc8cb96437e1fa30d7963118dce559ff`  
		Last Modified: Mon, 28 Apr 2025 16:55:35 GMT  
		Size: 37.9 MB (37887470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce9f57aa1d6908dcd943f34d1cb9f35acee0f7b2adadaef31267686265fc09`  
		Last Modified: Tue, 29 Apr 2025 17:51:14 GMT  
		Size: 28.0 MB (27986783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba9138fef356bbd33c4a1f66860ecccb6a575d2204f3a83a7473d8de038efa2`  
		Last Modified: Tue, 29 Apr 2025 17:53:16 GMT  
		Size: 143.5 MB (143520720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3b4d8b5def29f1e51716168ded619047c0626abc8fb37e1bb38edffa8c88b0`  
		Last Modified: Tue, 29 Apr 2025 17:53:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00a42cf5e6364f2acba7b444196cfa0912f459d8db1c9bcd01612baab90a5d`  
		Last Modified: Tue, 29 Apr 2025 17:53:12 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8efc07a71df7eb96d19d5fe0bbfe2bb74c43c8fee7804a75bdd145e007745989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa632223f42cc448ec5e84edd0e01f7f6e7375aee14d71ecde2de4b456f8a9d`

```dockerfile
```

-	Layers:
	-	`sha256:4a6b2f420d1559e1b6386245b55805856cd393ce00fc47f69569371f98b51a19`  
		Last Modified: Tue, 29 Apr 2025 17:53:13 GMT  
		Size: 2.5 MB (2454656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39804d6c97030ff32a483379e713266678f143d6db82a18b8b261c0d8ffb70c5`  
		Last Modified: Tue, 29 Apr 2025 17:53:12 GMT  
		Size: 21.3 KB (21273 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:cae1ea6fc912f1253850d63a431b8a594f7b8ddbb7bc576fc18fff24a78591f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218378454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfde85d3dab327fceffe21e6aea86b27866f0c250c089cc6d754d44780d6e5ca`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:352b288c8223eaef7c671c611c93e11c1f1a08ec40f3f05f199babc323ce9c37 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-04-28T15:57:47" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64le)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        x86_64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:e32416660495649b2ba0129e756351f46ec1023f3bc9594febaf780fbab240ec`  
		Last Modified: Mon, 28 Apr 2025 18:29:40 GMT  
		Size: 44.1 MB (44107495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b2f2feb522ede46945b0975b09aeb2bfb6324b3f69796498cf5a57bfc426`  
		Last Modified: Tue, 29 Apr 2025 18:41:13 GMT  
		Size: 30.0 MB (29966503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52b226088de9c09ef786bded67e52dbe9003f0792ba7c79141cdc4b74d77c88`  
		Last Modified: Tue, 29 Apr 2025 18:44:56 GMT  
		Size: 144.3 MB (144302036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b511182172956126322a97fd3fdc2de0ee6a86ecb993094b923be05570699b3`  
		Last Modified: Tue, 29 Apr 2025 18:44:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577b945e20d44e1a8bb04170a8f56ea4cbeb416f9fc1385ab4bfd97c1e7fdbe8`  
		Last Modified: Tue, 29 Apr 2025 18:44:52 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e6c284efaa7f20d51ba87a73587a9e4b3ab0a1edcdf92ac260d5216df42102f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63728df54588b59af7c9c421062ee0ce2252842ffb5eae26454847dc15755128`

```dockerfile
```

-	Layers:
	-	`sha256:85e735bb5e83f7c1c43fb4f8b7c893e7795d515d5135dfcdca0dbd09c744f945`  
		Last Modified: Tue, 29 Apr 2025 18:44:52 GMT  
		Size: 2.5 MB (2453378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db7014cc89595d1daa1a5fc2a7c93fee6533cf72270434524dd500c2f0eaaac1`  
		Last Modified: Tue, 29 Apr 2025 18:44:51 GMT  
		Size: 21.2 KB (21192 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3cd49ca3931474d5dd27ca6b5c5ee4b24a0ee43f6d567b2b851be68aa40ac2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 MB (200073609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5270cadcd4555f83add7ad71b21e5261c9309679cbc1c372c1873a3ca2d5910f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:bab1dba8fd7b792fd9c8b4d4831f07de632d98b60b25b5bfb612394258ecf142 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-04-28T15:49:27" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64le)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        x86_64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:0a17b1176e4d1360a16f39111ed35c973d6f8d1a50962dc023a27e6fbfb36505`  
		Last Modified: Mon, 28 Apr 2025 18:29:29 GMT  
		Size: 37.8 MB (37826548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2e3c1dd51f9b39a5b5ada87939c3015910952d0f3dbc5464d9be3b01b9fad7`  
		Last Modified: Tue, 29 Apr 2025 19:17:07 GMT  
		Size: 27.6 MB (27568807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b49f02026b05de21e5d750d101ee34b153e7436031de07244a697b74ac59a`  
		Last Modified: Tue, 29 Apr 2025 19:18:28 GMT  
		Size: 134.7 MB (134675837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef644a3ffc8170b12de198581cc4bba8d255ec05342417ecf1e71f728bff530`  
		Last Modified: Tue, 29 Apr 2025 19:18:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16186e83a7d927d901ccc7eb08010f1b78c9313b363bc52c0f13c5b7fb8baf0`  
		Last Modified: Tue, 29 Apr 2025 19:18:26 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4b79fce247c2e504e51f7d3e463eccabc22528f5e383b99a0b4cfc7f062c3618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2853e85b0291cb3e179add92ee5400bc8cb3dd1b2512cc92eecb58a554b2e2d5`

```dockerfile
```

-	Layers:
	-	`sha256:e365ca4869036fab731f8daa06040a9fd38a0c1bdd5f0ac493ca3eeaa68e8433`  
		Last Modified: Tue, 29 Apr 2025 19:18:26 GMT  
		Size: 2.4 MB (2442678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f283211f753a31e0cc218dca516160588cd5a59fd1d48543d9ba4cbcd792c46`  
		Last Modified: Tue, 29 Apr 2025 19:18:25 GMT  
		Size: 21.2 KB (21157 bytes)  
		MIME: application/vnd.in-toto+json
