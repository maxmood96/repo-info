## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:823e4456ac1522fd9a3c26be2fa469cde9fe7fc58ccde020143851588338d8df
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
$ docker pull eclipse-temurin@sha256:7721cd571da741efd4506eb854cafc5dc95b244ba538405286df5d9627932265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125623941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2da73c8a4ffac5e6b1947c82cec2e9c52212f8bd80da5bf4eb3dab67ed2a19`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 22:13:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:13:43 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:13:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc97bf791a77548708a538af915fe01451737cfb1597139c45cab6140876d7e`  
		Last Modified: Thu, 05 Feb 2026 22:14:00 GMT  
		Size: 30.4 MB (30394983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85317981b42d8c42b50cfa245808c0f5150bc11079f6ba7696c8a267311f94d`  
		Last Modified: Thu, 05 Feb 2026 22:14:01 GMT  
		Size: 55.2 MB (55170625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c0c44053fd6dbff25bdf9d51f2951536f621adeb69288b8236dbd9b80df62`  
		Last Modified: Thu, 05 Feb 2026 22:13:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36164708367066064518f78fccb5b6b6af5fa50c5b55094f65362feea092e2d0`  
		Last Modified: Thu, 05 Feb 2026 22:13:59 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6603791b76aabce9a559ca79670e7c1cd44a3869f19ced1f2a3afd176af2d220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960f664d014b58cc47bc2683d52ed9fd24d3ce2b1b49000bcc815421333cac1b`

```dockerfile
```

-	Layers:
	-	`sha256:bf9811d7f18a468af2593ce09236bc535d1c5c88a0ae268cd3a1e3f4492bf742`  
		Last Modified: Thu, 05 Feb 2026 22:13:59 GMT  
		Size: 2.6 MB (2621145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa47f188c2d520bf37139e1ce660167de6ec0c214650d94cc4f44e222332e42d`  
		Last Modified: Thu, 05 Feb 2026 22:13:59 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1daf2da24ede1068be6ae290c97cfa54b3fca0f2f9164346022aba1faabac442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123300377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c943377805c012c0b633a9b1dd38b0ad93bc0bdaf8b1879d2c6447b86a1119`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 22:13:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:13:45 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:13:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7cd8d2b1f49bcef55b9896e6394b936b78704449a78f01b43bfdf2d814cc9`  
		Last Modified: Thu, 05 Feb 2026 22:14:03 GMT  
		Size: 30.8 MB (30830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d325127322a77f3c43c4c621ff9816ec62be861ee4b0c497d92b708462e62ce4`  
		Last Modified: Thu, 05 Feb 2026 22:14:04 GMT  
		Size: 54.3 MB (54252012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db194e18b9d57e6cd8e65cbb80c50c93ceee62288c0b12d9928e6b24c3626f9`  
		Last Modified: Thu, 05 Feb 2026 22:14:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e2ac8bb99c765707667cb3858b0ee7dd4df61322565cfb639bd21f55ba0927`  
		Last Modified: Thu, 05 Feb 2026 22:14:02 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:49dbe4501331971b3045c4b9124e57be0c8c3b573dff594c5ec997deb8f131af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee215178d1d1a85e0ace43ee7c1474884e1fee8a70c7ca1a01b4532f06f364f`

```dockerfile
```

-	Layers:
	-	`sha256:65d03c21f8a37ef01c0b738ec47e5331ea737df17018337af5b4707e7920952c`  
		Last Modified: Thu, 05 Feb 2026 22:14:02 GMT  
		Size: 2.6 MB (2621215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e85259a1a5b38481cd02f0d4ee67714eb40f71ec0e78ecacb347d1297f13ace`  
		Last Modified: Thu, 05 Feb 2026 22:14:02 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e47dc5d61334d89609669f02fcdbb93755e2d8445477be695857b6734a807647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129990795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87825fdb18d2410704fe152fd248525aa16603d7c402167af7ebc9b04eb6683`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 05:19:59 GMT
ENV container oci
# Thu, 05 Feb 2026 05:20:00 GMT
COPY dir:88b5851a77c5a8923c1135eccf97b07bb1b1d533881d05c9e3cd86d6a7a70b84 in /      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 05:20:00 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:2deeab01ced2f311ec55a8229431b4137952c26bddd647f35c23005dfebf307c in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:2deeab01ced2f311ec55a8229431b4137952c26bddd647f35c23005dfebf307c in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:20:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T05:19:48Z" "org.opencontainers.image.created"="2026-02-05T05:19:48Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T05:19:48Z
# Thu, 05 Feb 2026 19:47:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 19:47:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:47:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 19:47:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:47:50 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:16:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:16:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:16:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:16:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4626d1a4e0f331b320f43bc1ebbec9d324207923aa2afcf48e14cccec11d1caf`  
		Last Modified: Thu, 05 Feb 2026 06:10:00 GMT  
		Size: 44.5 MB (44461525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8721df182f63163a820ae421087a60cd6792f46abb4eee0680081557ec55653e`  
		Last Modified: Thu, 05 Feb 2026 19:48:35 GMT  
		Size: 32.9 MB (32875919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa54f458e3485c2a9989dd5e09f90ea0ca4d9e4a0cfb0257017174e9058e0bc5`  
		Last Modified: Thu, 05 Feb 2026 22:16:38 GMT  
		Size: 52.7 MB (52650909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeee482242db253b1a169af0ac696dfe526022d78f90cebc0c84a8e1fb8f233`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f7273a9d9be127d2e644ab4277a07a69ed8be2bee9f170a1c48b57759f83b`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8ea5575a7cc3d271bc765e55e58242f0f9258e70992e54ceac7318fbb0654a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704131210f9a5a55ee191ea866578b73854efcd8af0465c535bc7bf440e9f8d`

```dockerfile
```

-	Layers:
	-	`sha256:0d1b005e95c92006c769fc79a92e9a4ecec7222c5a34964ae6a1490290be2d67`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 2.6 MB (2619832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5567d0519a293dd0142e03fe4a19946282f171bd34df42402c668b002735984a`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 19.9 KB (19909 bytes)  
		MIME: application/vnd.in-toto+json
