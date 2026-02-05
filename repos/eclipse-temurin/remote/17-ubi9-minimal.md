## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:53ea2421ad0c10e06fb224933581a3d55b1da883a121d57d9e70a41c9f6c4447
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
$ docker pull eclipse-temurin@sha256:5dd940580805da45f09f8f2199fd15473a974c4f532fc6bc69ad96cac0ea2080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 MB (201111107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf74d96b03f6997b353fe2b588d41d0bb13c7770e02be5bee9475d22bd62e5b7`
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
# Thu, 05 Feb 2026 00:08:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:08:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:08:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:08:08 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:08 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 05 Feb 2026 00:08:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:08:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:08:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:08:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:08:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa04d2332b3dbff85f3bed3e58efa02aee9a199df69ab62f29c7d473cc2f5ad`  
		Last Modified: Thu, 05 Feb 2026 00:08:30 GMT  
		Size: 16.2 MB (16246753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d7bbab115de95cc957185a1ecb153e4f5e8077fb284a74b0f25a41d8ea111a`  
		Last Modified: Thu, 05 Feb 2026 00:08:33 GMT  
		Size: 144.9 MB (144852876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b5754b26eebb8a1c4b7472f0dbdbc6a723a01e1e50af89f137173afb4a574`  
		Last Modified: Thu, 05 Feb 2026 00:08:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f25cbb074b5978cc1e42bcc21057ba5dd7b28920c3402a6577b62bcd09e1f9`  
		Last Modified: Thu, 05 Feb 2026 00:08:30 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7dabe99701302cb3b04b630d2a870553d4d4747a60a1b4b533145bde1be89abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1780646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeca945dfd5088c1b44bbeb17c851929446d7dd936bd9e51c0d71d94bf55b01f`

```dockerfile
```

-	Layers:
	-	`sha256:cbfb2374c6789b3ee44c7e72917bad24c0742a7463225a80144486c5cc5ac6a6`  
		Last Modified: Thu, 05 Feb 2026 00:08:30 GMT  
		Size: 1.8 MB (1759478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81015956046944b9973955685e1fc6a59c377169721b28757f326a6219d14c30`  
		Last Modified: Thu, 05 Feb 2026 00:08:29 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ec2861bbd7b35d5c2bc853bc566b955198f115d99695c05ba0476ea54e861e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198668036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a18bcb6d0fcd513b5b14eeb8b56095338562738cb389e878887f4549bcb8e4`
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
# Thu, 05 Feb 2026 00:07:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:37 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 05 Feb 2026 00:07:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:07:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:07:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:07:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:07:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4833b42136e647a2a7eff386c41e50b921a05c6184fdbdc68ca389c7115c091`  
		Last Modified: Thu, 05 Feb 2026 00:08:02 GMT  
		Size: 16.8 MB (16784505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e614d718651ad52d5ee9cec5340ea99f651f1b927390d50bab56259dad8040`  
		Last Modified: Thu, 05 Feb 2026 00:08:04 GMT  
		Size: 143.7 MB (143685391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b4554d21a988c3afd2d7419b954851dbc619fe833ba1b59c27bf4d316c202`  
		Last Modified: Thu, 05 Feb 2026 00:08:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bf309db97f42baae3b4a6ec4dfbf557eeb9a7208c34c032c945f2ea471012f`  
		Last Modified: Thu, 05 Feb 2026 00:08:01 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:02efcddf26a6ae1c6eaa602bc9963d7685dedead371ccaef21bdc04da5fca383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1781361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59144aa52501f751750c408874ce124146c87cdb8f5450841855cf38894e8bb`

```dockerfile
```

-	Layers:
	-	`sha256:c1fb3ac0c1df2a5ad2953424cf6a96936faca7963c6a971af558e2eba08942a7`  
		Last Modified: Thu, 05 Feb 2026 00:08:01 GMT  
		Size: 1.8 MB (1760078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fe502a0fb8e0fab2f01a039f59534d937547ee3269aea003abe49f15e9ef2`  
		Last Modified: Thu, 05 Feb 2026 00:08:01 GMT  
		Size: 21.3 KB (21283 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:6dd86da9568d3212c92bc4f3cba52a5789d9106bd70cd1ead459ffc5ae532509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206936410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24824e4180ad443553fa0bd339e872789bb310778cd47a86a92f959249d9a504`
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
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 05 Feb 2026 01:25:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 01:25:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 01:25:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 01:25:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 01:25:38 GMT
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
	-	`sha256:d964c541856e5ec8c146d2ef2d31f1df6e8d4d4c5cebdcefce4691aef64d17da`  
		Last Modified: Thu, 05 Feb 2026 01:26:18 GMT  
		Size: 144.5 MB (144547640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a96fac8e89f5b62eccbddd57a40dd86995b8a6613b33a6adad64bcc2f102057`  
		Last Modified: Thu, 05 Feb 2026 01:26:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86cd2338cc43005fc4039812e1ab449ba34f4706e976a00815418a144d6053c`  
		Last Modified: Thu, 05 Feb 2026 01:26:15 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e2c0b9ff3df2bde8c5c6b91c71f173326f3a8593c1fac00210e0c34b045776fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1781186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f713107c560736c250e419c00cac933829241b4e2f2da95ef5e5e124aac1de59`

```dockerfile
```

-	Layers:
	-	`sha256:00a02d9270d337c810000511e1b8dacc1f99a758a8caf2b824a1764e80269bbf`  
		Last Modified: Thu, 05 Feb 2026 01:26:15 GMT  
		Size: 1.8 MB (1759982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff5c7a6bc6d722da4240b79d15fdcd98d414d7e9c391d7d60f2387af3b6909e7`  
		Last Modified: Thu, 05 Feb 2026 01:26:15 GMT  
		Size: 21.2 KB (21204 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:41157b65419de9d3ff1ef38e078516728387684b3b857b546c922f3a1fe4b77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189608435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bb4126ae16dffc50f3b1a80ce4d80f344721996026955d2117bd6bc77a39f3`
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
# Thu, 05 Feb 2026 00:07:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:05 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 05 Feb 2026 00:08:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:08:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:08:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:08:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:08:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3073672938ee024c2e2b6308a166357e08b9d63db19f1301982940b3e05b9c5`  
		Last Modified: Wed, 04 Feb 2026 12:09:20 GMT  
		Size: 38.1 MB (38133403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c4bf4a29d40e5c4b0c1fba4adb6997451da9237b42a8a607dc0aaad11359ba`  
		Last Modified: Thu, 05 Feb 2026 00:07:32 GMT  
		Size: 16.6 MB (16610440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc09916d9b55552496684d95ecde38b06b82a696fbcdd870784d7997ac7bd21`  
		Last Modified: Thu, 05 Feb 2026 00:09:11 GMT  
		Size: 134.9 MB (134862173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c6eb12d5458bae33861e7cfcad165840efd98b59add5e5e559fed30bb50afb`  
		Last Modified: Thu, 05 Feb 2026 00:09:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8131e518094a502cf3649e5610a0da48e92e35b37331f081e4b34bfe1fedbc47`  
		Last Modified: Thu, 05 Feb 2026 00:09:08 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:28d46c9e4cf091ae775f45011485052036c1fee67336adaec3079d6b7c37f7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1779908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3fef917881e38dfcfd2c55af7d34c47cbb0cef9ee7d29e4d554f82cca5c776`

```dockerfile
```

-	Layers:
	-	`sha256:3cda061afaaccdc58ba5c243ba42df7f5d94348026048541cabfd1f8079b2ae8`  
		Last Modified: Thu, 05 Feb 2026 00:09:08 GMT  
		Size: 1.8 MB (1758740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096d061c63f4983e552f4674fddaa2b36bcd54ea0d1ab66ecd31a6bd0e9ef1c7`  
		Last Modified: Thu, 05 Feb 2026 00:09:08 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json
