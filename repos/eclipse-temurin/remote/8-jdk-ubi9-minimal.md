## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:0192dad028fe5aaa0654ed195916dd3307e75db6be0e4c215b53342cccca831c
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
$ docker pull eclipse-temurin@sha256:a3999f3365ff27518dd571ea3d00c01af108edbe3a31e53d2025045fa0926770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123574682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98acd55c3184f8389c9d85473a652c919424724869c873b09db7eb1ee48b82d4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Tue, 26 May 2026 23:09:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:50 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 26 May 2026 23:09:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 26 May 2026 23:09:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:09:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:09:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c5e556662167a71a554f6a3aab7c55dad930cbdb297734596cda3faca9d6fa`  
		Last Modified: Tue, 26 May 2026 23:10:09 GMT  
		Size: 27.7 MB (27664234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce79f3ab3768725816479ca901a7e9ef7ac0745a9074b040657a0fba13b576e`  
		Last Modified: Tue, 26 May 2026 23:10:10 GMT  
		Size: 55.2 MB (55199135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3da61d38eca49ad93f4325f7583fa8015bb8a0c67e0bae245d35c9c77c73cd`  
		Last Modified: Tue, 26 May 2026 23:10:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8fb45750fb765fe40b198d2c4dea86a9e5672cdb9ea835cd299c0338817c00`  
		Last Modified: Tue, 26 May 2026 23:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:730fe6ec65ae61f24a7983b823a53b1479c6fc000cd5910de67fab68dffac4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a3af5d859463810805cbd21678a8b5ac20723556ffe24e3f38649d826cb6d6`

```dockerfile
```

-	Layers:
	-	`sha256:e950ff19a16b27538aa5d4b1e263d665f2f83ee9a68e97ddd4531767ab48679f`  
		Last Modified: Tue, 26 May 2026 23:10:07 GMT  
		Size: 2.6 MB (2615450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76dc1105b1a232b4e31ac8bccce8d21890a9dd26f5f4a329ff823611ebb418aa`  
		Last Modified: Tue, 26 May 2026 23:10:07 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1dabfca96664c28f4531e0658986f2639188789ec169bf0797ef8be9aa74ccc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d1a3e00fc6b0fb86b12f961e3d6cf9de806b4e7a91c8cc92ce3f52881ce440`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Tue, 26 May 2026 23:09:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 26 May 2026 23:09:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 26 May 2026 23:09:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:09:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:09:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5508350f291e5f1f937fb0610ad086d4ac4585d1eac3624a15ca5541c7e14aca`  
		Last Modified: Tue, 26 May 2026 23:09:44 GMT  
		Size: 28.1 MB (28098710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7d02a5a41edafe7ff52011d81e8c896ca8ca8a58938dd4dcb2f7c2384acd2`  
		Last Modified: Tue, 26 May 2026 23:09:45 GMT  
		Size: 54.3 MB (54273431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800f7f427174438ccf235d276d8fb12497b09a5bfee0cee6717332b6d8260f35`  
		Last Modified: Tue, 26 May 2026 23:09:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9838193281c3fc475221acd64dcc6baf0379868b18aecd3b17e4dbebcae4a03`  
		Last Modified: Tue, 26 May 2026 23:09:43 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e7d172f40ded4dc1c2f5350a08556a559885e5e56e79de53a67341f2c2ef4dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bd9133cb58e7358ea3a5773d6cb190d5e5bff3eacfb1db71650fc05f2fccec`

```dockerfile
```

-	Layers:
	-	`sha256:81f283af7acf1810b9a8c45f4869ecc60923e1866d49fecb2aec40b5f832d447`  
		Last Modified: Tue, 26 May 2026 23:09:42 GMT  
		Size: 2.6 MB (2615520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2c6ff466eec13d84c53951b5f5c282a6e9bc75a667b1073fb614301b47ed3f`  
		Last Modified: Tue, 26 May 2026 23:09:41 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5c7ab57ea89625439d3076849dd008de006065d76fe145dc61bbfd4d8fd24fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127937841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4fe672dbe35b0bb91f9983a70bb063302d69bdde6d7318eadbe710d084be02`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 15:33:29 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:33:29 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:33:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:33:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:33:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:33:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:33:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:33:29 GMT
ENV container oci
# Tue, 26 May 2026 15:33:30 GMT
COPY dir:5e813a184cbab7cbf1fee0022ee8e55aa80387ef4835bad3a6804243f83209e4 in /      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:33:30 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:33:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:6f186cff34757f21b3d3a096028791fe755881607c0652e8eef706352323f06b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:6f186cff34757f21b3d3a096028791fe755881607c0652e8eef706352323f06b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:33:30 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:18Z" "org.opencontainers.image.created"="2026-05-26T15:33:18Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:18Z
# Tue, 26 May 2026 23:08:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:21 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 26 May 2026 23:08:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 26 May 2026 23:08:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:08:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:08:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f263dc8aecd57a446632c1e9df773e64bf709523e5ba6125cf199c6099e78689`  
		Last Modified: Tue, 26 May 2026 18:14:02 GMT  
		Size: 45.2 MB (45170860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb610a3d89ec570af77bbbb3ef8a428aab0ae8be44919b92e068743a6d993703`  
		Last Modified: Tue, 26 May 2026 23:08:56 GMT  
		Size: 30.1 MB (30094662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b60e9f4084ebdbab122f1c545e75f340f3d507c1b55e10eb458ac66b7ebdb4`  
		Last Modified: Tue, 26 May 2026 23:08:58 GMT  
		Size: 52.7 MB (52669701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce48cb3b77e410f8fef752a199f282c2dd59aa9ab84b07e84ac5a44a7574483`  
		Last Modified: Tue, 26 May 2026 23:08:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f653c0a4aefaad96a45db30ef4df064deb635d814a3161ec9097a4489f0d358a`  
		Last Modified: Tue, 26 May 2026 23:08:56 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:078997cb52a77e7eb81e7597aee03941b68c5d7e9b1247221813fdc9085f3f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8a9d04dcad9a6bfb8c17b8bba06350edc56611c1b32e78d2ef0d6437c988d8`

```dockerfile
```

-	Layers:
	-	`sha256:568b72c1d026edf6ac75cc251e7883adab7a74b07540e42914a0af94537f3b4c`  
		Last Modified: Tue, 26 May 2026 23:08:55 GMT  
		Size: 2.6 MB (2614175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d3597fc76f7c104c8792def1eee6d83a0b009c241148ef16693105304392db`  
		Last Modified: Tue, 26 May 2026 23:08:55 GMT  
		Size: 19.9 KB (19909 bytes)  
		MIME: application/vnd.in-toto+json
