## `eclipse-temurin:24-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:c23721e2a63f61bcbd4908a7bcf306b046be17c69585f45a211c2a424df14d2a
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

### `eclipse-temurin:24-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9d27b1ad33c84cdf65800512d50281a1bb53d8d4a372f5bf4138f80daca94b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178565917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8875fe38890fc8f86e4f56af3452b392bec92d5e5190f816765b6b274fa64f47`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:d7d46744a920e661eed10a42e2080d8056941b338e371ab560c4c2eee7e7a070 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:2c9300aa2a82321bdb1295eb5cf59270c200f77d73b01c9b866932f5e4bf93c1 in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:00:12" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fe33f3d694b6e20455a988c4bdb920e5a216d54c81a4c79494b6d0debd58f76f`  
		Last Modified: Fri, 08 Aug 2025 00:12:36 GMT  
		Size: 33.5 MB (33498072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37c060619cff7c8643dd9ab42f667ccb3a968599bc5336ebf7a27a6f9aacecc`  
		Last Modified: Wed, 13 Aug 2025 23:02:52 GMT  
		Size: 55.1 MB (55091183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb3ab6986452c99de3613c03aa6662f608416ff95a5a3f2ffb88038e5b87f69`  
		Last Modified: Thu, 14 Aug 2025 02:43:19 GMT  
		Size: 90.0 MB (89974243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359dc5f5daba618664857c15e5867a7916767a66a5b9b06f8759934b0cb6d20d`  
		Last Modified: Wed, 13 Aug 2025 23:02:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbb0c3b4f0700a403303e981019b4c1a3219b48a219894e9e3f6b1bce9af728`  
		Last Modified: Wed, 13 Aug 2025 23:02:18 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:634c3793ef70b4114b626b942e94f66431e61be9664cb363e1b6597ef79e907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fb4c7a0141cf018cd0ec47f09c29f23ab3d5af49244b6e0dfea44ade8e1f95`

```dockerfile
```

-	Layers:
	-	`sha256:365b1915356c6e8bab0749f9d16085d7790801170dccef178e6c3a75096122b4`  
		Last Modified: Thu, 14 Aug 2025 00:15:48 GMT  
		Size: 5.6 MB (5624597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c4b805c3831619991c2c7b06826bbc318237e7236d6272f5a979df43c332f2`  
		Last Modified: Thu, 14 Aug 2025 00:15:49 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:319f81f43abfb15299438aa56f15d914c60db8b146ed8233ee4ff7535a43b79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175512121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6b0f8f254009ab6942147eab91fff895fcfe385e6042dac954d2b24cda0363`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:8385fc5490591ca16c81e8d24d20265b9384f30798583b224537cb1d56b1a850 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:06:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ed98dc7fc2264d2da8c020e12ea4548801fafd192d4c74444ac087ada4c6d75`  
		Last Modified: Fri, 08 Aug 2025 00:12:34 GMT  
		Size: 31.5 MB (31546088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0156aa0baa8f8522aa7e2a1820c735e597ad956ddf096f06ab53a2967160bae`  
		Last Modified: Thu, 14 Aug 2025 10:11:05 GMT  
		Size: 54.9 MB (54863066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1def34fefcfea09dff5d8ea43ba47db9ffa5e511f1d7bb84753c79c41bf4c42b`  
		Last Modified: Fri, 15 Aug 2025 01:14:05 GMT  
		Size: 89.1 MB (89100545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76052e10228be3c3d557237954e1039e5383ba088b0236bb7800525309eb5aa`  
		Last Modified: Thu, 14 Aug 2025 09:58:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a2966434aa1c95041e5e1df77c11b034fce837aa134312bf0154d6c56125ce`  
		Last Modified: Thu, 14 Aug 2025 09:58:22 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:51c90e47fab65cf381c40bdd0316aa38f3075cc0996c17f2f0322001311ac25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d155131636b1deb675c5562a02c676015f18e8dfdf18e6d9da53ff81a96d0d14`

```dockerfile
```

-	Layers:
	-	`sha256:a446609406be7278ccf3024c4e568fd58d4638fcf2f6974b1343e30c048e119e`  
		Last Modified: Thu, 14 Aug 2025 12:15:58 GMT  
		Size: 5.6 MB (5624084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd096daf0977c9be4c03d3db64448af16b990d06000a15ac3aaaa6693c155d9`  
		Last Modified: Thu, 14 Aug 2025 12:15:59 GMT  
		Size: 21.5 KB (21472 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5365850f56a04203c0094dab9f0006186b46d337bd9b9a7e1098ca30cc26e472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183837884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b118ecc4f2d2e338be182bcbeb13ce530dd67043fbbeec341787473abd7088`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:640e0e573d0fea25191602587d27a678361464a59a51c46e7e2ad55c65a20739 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:14:08" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fbda37dec747d2d48a0b731bbc4647a80d0ad38995d3e592715932bca71e095c`  
		Last Modified: Fri, 08 Aug 2025 00:12:35 GMT  
		Size: 36.8 MB (36811145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624c78cc03453e81963d16cbd8cf44b57233f3676f5c0b5a6ae9b680b7e1aca3`  
		Last Modified: Thu, 14 Aug 2025 04:45:35 GMT  
		Size: 57.1 MB (57099241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fab03098ff698de40bad71d099705ee1f898f56fc307529e1eacc0bfc3a2e8`  
		Last Modified: Wed, 20 Aug 2025 00:58:06 GMT  
		Size: 89.9 MB (89925077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb286d5f5d1fc2083d4d188c8710c46e40174c66ae49942713ab9ac9410482`  
		Last Modified: Thu, 14 Aug 2025 05:38:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b18454475e893fd1f3bac2b1ef5e4aa6eaac03b7ca734052e3195f55131922e`  
		Last Modified: Thu, 14 Aug 2025 05:38:41 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e9194d3e72724e59880dd9e8eaba3d7ac34321725e183ec3e3037359febc3b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5634439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a30ddb643dce6d3ba95bbd523907fd411f67d02ec603e54036cd039f75c85ec`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b4001f698ef56935769a59dfeb70ab91d71779e6838cf096e0a3bc6a237a9`  
		Last Modified: Thu, 14 Aug 2025 06:16:19 GMT  
		Size: 5.6 MB (5613047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b480c4b017caf80f1105fd1b924b93e4722cd1d96dd8630cdd9011f9dfe7fe`  
		Last Modified: Thu, 14 Aug 2025 06:16:20 GMT  
		Size: 21.4 KB (21392 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:65156f197739afcd1c545d01a250ff372e620233bbdd69c0485f575de75be942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174314266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dad32deda3a4fff1782c09c5e9d2ef1fcee85aaa6e26d12154380ff67b3a4a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:bb8541e617ae72e609facfec80e743cc4f049732f5a1f4acff90ff475615b5e7 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T19:09:07" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84d3bdaa36c0d56559b106975b26dde8bdf88341585cb0bf151bc1ac5c802c23`  
		Last Modified: Fri, 08 Aug 2025 00:12:36 GMT  
		Size: 33.4 MB (33411761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4608aad02821a2c4ed1f8242350611f4dd6e9c2061ab67d2b52b6786fc2bc728`  
		Last Modified: Thu, 14 Aug 2025 03:59:46 GMT  
		Size: 55.7 MB (55673689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e08c671c01278813586e1ae9d607a3c1fb8514a8a0411acbe31e050849203c7`  
		Last Modified: Wed, 20 Aug 2025 00:58:06 GMT  
		Size: 85.2 MB (85226396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038a8e650821dd315a53d53c685b1b32e58a21009258e0c60085aa9444b1023b`  
		Last Modified: Thu, 14 Aug 2025 04:08:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42e80919cd3d1e2093be910fe457e288c9e23e6fffb61da70fbce86c852b5c0`  
		Last Modified: Thu, 14 Aug 2025 04:08:31 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e6bc440dffa1321cc330c3c226af647d17d99568c38d3200fe37547e04b9c88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5634026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b18bc47d6bf01d338ac0260788d6e9fc493d141bc3355fe6bc4469b3e5dea30`

```dockerfile
```

-	Layers:
	-	`sha256:10b7b68da00210c45a289f1127b758a95f43de0574adc1fe0b144cef2927ecc4`  
		Last Modified: Thu, 14 Aug 2025 06:16:25 GMT  
		Size: 5.6 MB (5612671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf06e799d9749b530e2ff25a1639ea2d92fdd06e612e851290982c7b719e677`  
		Last Modified: Thu, 14 Aug 2025 06:16:26 GMT  
		Size: 21.4 KB (21355 bytes)  
		MIME: application/vnd.in-toto+json
