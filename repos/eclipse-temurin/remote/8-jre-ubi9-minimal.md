## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:314801d9441a5184bd4d5c65ffe6fe7e93ef7ca569892825926c2fb60403cb2e
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
$ docker pull eclipse-temurin@sha256:f0c452c7c3ef19285a115484bc4b06ba932195514c8ee904d8276df30b79ff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118300743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b715ce2ccee541547e661a7c90a61636657033b5e825c7388f5d200fd6e4052`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb307380727252ff082f6e19334e3ec8a99bc0dde77bc6fb25b8bd72830ca6c`  
		Last Modified: Wed, 22 Jan 2025 18:27:56 GMT  
		Size: 37.0 MB (36987590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60956aa87a2f5a2d13864e18c9c346beee51875b99a34f4cdebf9b28f386cfa6`  
		Last Modified: Wed, 22 Jan 2025 18:27:56 GMT  
		Size: 41.9 MB (41877910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a5fbf44b12e3e65d7f5b48966c3bbf7c6e4559d6ead2bcaf853059b856562`  
		Last Modified: Wed, 22 Jan 2025 18:27:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6886763a00bbafa474dc41cd6a503082b07131da66e5ff37c019ebc0f0b1f9d3`  
		Last Modified: Wed, 22 Jan 2025 18:27:56 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:646dfda2e55b7bf07fe9fcfbb0de6f572801632bfe5411994e36c3c0f59f8a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c89dc4bbbf25bcb1718a7da93ef2cd01cfc589a470e2612468de53d9ac1536`

```dockerfile
```

-	Layers:
	-	`sha256:21c3754cbccc952155fc31408035bfb624f2ca828051857791f92a9ad77d3401`  
		Last Modified: Wed, 22 Jan 2025 18:27:55 GMT  
		Size: 3.6 MB (3612424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61cbcdf04f8bee8234ba92a41a2ac6a22807490201178f052191169fb13fc722`  
		Last Modified: Wed, 22 Jan 2025 18:27:55 GMT  
		Size: 19.9 KB (19918 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1c8df43069a47f28189814f31c4a0d1ac6001398e1cebb4737a0484c4301e1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115884627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1bee84f255aeb6f64d14c80db552fc1de1566fabfa35bcf813d279b8bdeba9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc249bdcd042886f9e42f55ca1acbc155028117c6226b2cd68dd2d0b94af56f`  
		Last Modified: Wed, 22 Jan 2025 20:54:17 GMT  
		Size: 37.4 MB (37443876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bf293c79ce61aeeedc79ab1965caa84b05208d9b9c21a4317fe891872b68e0`  
		Last Modified: Wed, 22 Jan 2025 20:56:11 GMT  
		Size: 40.9 MB (40860511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3244cccfccc404eb75544b17fd01c5a5db6821411356d73c3a32c4f1206992ab`  
		Last Modified: Wed, 22 Jan 2025 20:56:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26496838b9b444770ecbd173bee8f653e61ecf0d8283b72db526333f14174e8e`  
		Last Modified: Wed, 22 Jan 2025 20:56:10 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7b6aa5c16187a9b701d3464b3531e3ef59864e34211ed7601245572743cfeefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2503114e97b814c166e9d28ce3d952904dc0e65a08502ce3b74f4cf1f624b632`

```dockerfile
```

-	Layers:
	-	`sha256:32acdb907093119292c5f08bd5dbe62e05b93f46b919db3b5744cde0345f31f5`  
		Last Modified: Wed, 22 Jan 2025 20:56:10 GMT  
		Size: 3.6 MB (3612293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0306dc916ee0580c86e4d80bb624ee7b5f1a57552d3aafa43a16a7b4fbd7706b`  
		Last Modified: Wed, 22 Jan 2025 20:56:10 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:83854e1cb5570876750d3694e35a4f08a8826fb8fa0efe43c8906d000d439d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124520480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09dfe0315c91b376fc25bc5ed6cbeb9fe374fd6db9e079512d0af5550d17f28`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:59 GMT
ENV container oci
# Thu, 09 Jan 2025 06:42:00 GMT
COPY dir:d7227f71d224f4a0ce6e41e096c5f35be3bfb0d1cc57d5e656694dcabcc752aa in / 
# Thu, 09 Jan 2025 06:42:00 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:42:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:42:00 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:42:01 GMT
LABEL "build-date"="2025-01-09T06:41:34" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:42:17 GMT
RUN /bin/sh
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:dce878563f15050dbee433ee11b302dc91caccb7bbf30b63a4d16c18ac4571ad`  
		Last Modified: Thu, 09 Jan 2025 12:32:39 GMT  
		Size: 43.8 MB (43794360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e8d75484ae7e9cfff00aa310d4197973e5e690156a92349511c158be98059f`  
		Last Modified: Thu, 09 Jan 2025 12:32:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18197cf46ebd87e4c786c45f34ea15620d00514afdc79daf54b112ed798a5efc`  
		Last Modified: Sat, 11 Jan 2025 01:35:09 GMT  
		Size: 39.5 MB (39476434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bde2cbe6ca98bde48f4e1d893de3054fc3eb961692af6de972ec1a41ed7e0ad`  
		Last Modified: Wed, 22 Jan 2025 18:34:46 GMT  
		Size: 41.2 MB (41246867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122e35f7b6de9169703034040dcee12fd15f992ae8c9798103b502ba70a58708`  
		Last Modified: Wed, 22 Jan 2025 18:34:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb16028bdf12feb2faef8b27bd2f48b22b61335af2e1cc81d037d83ac3083659`  
		Last Modified: Wed, 22 Jan 2025 18:34:44 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d738280d072c36a264616d66b5f0e3e62ae61ad3d24a700efb36983e6fc8a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b128ca1af3d58ff70793f13a897a2695ba6c5993013fe7de7cc04144b3735801`

```dockerfile
```

-	Layers:
	-	`sha256:e6998317c740e66f6d2addd741763a38bb641f3ce2d08688a5c48c4385ca996d`  
		Last Modified: Wed, 22 Jan 2025 18:34:45 GMT  
		Size: 3.6 MB (3612940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56648b198b2af76eca838f855e3cf9a34acb9f450adef60178452b8046843033`  
		Last Modified: Wed, 22 Jan 2025 18:34:44 GMT  
		Size: 19.9 KB (19948 bytes)  
		MIME: application/vnd.in-toto+json
