## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:9df81918eb90bdd69c670a0a9427ea5f6c57077a5974d9b60fd2792bef86bf06
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

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e7298019c285d8a207bb6671d740c0aeb3989ae6ee03a7f6aa3e35d2f307686a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121497583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bcf430dcce7655ca9ec6b01894c648fe15652e98b950e7a31ffa662a154a84`
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
# Tue, 26 May 2026 23:10:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:10:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:10:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:10:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:10:47 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 26 May 2026 23:10:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:10:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3726a786484556b9c1b8fc9e0a3e4a2589b8376af1d9fcffa15ea0bd9e5d6346`  
		Last Modified: Tue, 26 May 2026 23:11:04 GMT  
		Size: 27.7 MB (27664196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43786a7b8ae1c1944eac1c896fb05ec4a7c4a96a3e4e3d5b60dfb1e698d47a29`  
		Last Modified: Tue, 26 May 2026 23:11:05 GMT  
		Size: 53.1 MB (53122272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fd779602987574388671f89e668f832065a9451003c84c5ce21732763e914c`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da59f03f293200cdc4ea499b527e74cefc987306a7440c89ca96f67ae0143f`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:243c34040089bfb9acee3bef82b22bd1c7509d62ee9ece642e201a88a23a8827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9de1993cab179107386acc8319041fbcd478381847f1aefbe070bf468f438c`

```dockerfile
```

-	Layers:
	-	`sha256:9007be1e581b222fab814034dce87b6e1a3c1365b18888d917908fa687e802fb`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 2.4 MB (2411857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50041a5439bced79d93257e7eb29f4937ce3391ae4018519bd96fcdc8701aac8`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 20.2 KB (20210 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6baf21987048cd4ea862722526dea14392675adae3385caa3a296d660a420277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119250560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac656530ed46a01b6cd05208f76f1878fbe318b8dac606900d106a01e91ad3a0`
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
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 26 May 2026 23:10:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:10:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:18 GMT
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
	-	`sha256:086b813c2eeb9976b5b34cda1c261992fc72a580decbdbbf1c9b3da0d09b1927`  
		Last Modified: Tue, 26 May 2026 23:10:31 GMT  
		Size: 52.3 MB (52309275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d3b88e06e72661ab9f28a6a62bd971ecb0eba52c9cdac0e65c99262685ef77`  
		Last Modified: Tue, 26 May 2026 23:10:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f961a640929df2c8bf6814c25d59b9e5723d46c29a07568345fb4a0b018b08`  
		Last Modified: Tue, 26 May 2026 23:10:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5c0a4267e6868ab67299c80f972af3e06bcb3af386fc91fc19d66eac5f2fd437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552b9e6924bae2b15d1057a45cabee3303366b1d678509cfb6683cae5551035f`

```dockerfile
```

-	Layers:
	-	`sha256:1f15cbb71bdb63d964bf2c33eef9c0cab9f74bf96ea5fae9df34a7a6ff6b5c45`  
		Last Modified: Tue, 26 May 2026 23:10:30 GMT  
		Size: 2.4 MB (2411215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4fbf97b272c4c698b06ba2a11eb52302cec378046f695ad882359bb6e122ef`  
		Last Modified: Tue, 26 May 2026 23:10:30 GMT  
		Size: 20.3 KB (20314 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4a730436189d7e57e63e82e782c719e466e306d0cb588a5bcc170eab7d819f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128406363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf4e697f1504c8ee689eb5e283d3e8c9813027d75cbda8d6162a7684c699332`
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
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 26 May 2026 23:15:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:15:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:15:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:15:04 GMT
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
	-	`sha256:bfeeb5911f1a4dfb718f6c3c0260168fdceb19bdc665b50a7e3a6e277eca055e`  
		Last Modified: Tue, 26 May 2026 23:15:40 GMT  
		Size: 53.1 MB (53138421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7958eee5e7477c5d2b63f80766a54f8d70557412a85367d97376b723fb8b8ae2`  
		Last Modified: Tue, 26 May 2026 23:15:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6294fa8e4ea9d9c2052a708ac8ea63477cf42e7da3d8ab15eff27c09745e07`  
		Last Modified: Tue, 26 May 2026 23:15:38 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:63351b7c5560c661f4070b6f5cddef0ba07aedcb68df91e05f1848c7ff6b8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3674e30c307f080e18543c80381a15852b63a006b1ffe817f46f5812a04aa9bf`

```dockerfile
```

-	Layers:
	-	`sha256:757ee1e8ba109bb1dc45121533531f05fc2e57eaa725400c60ef0d6d93561cce`  
		Last Modified: Tue, 26 May 2026 23:15:38 GMT  
		Size: 2.4 MB (2411900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f97b85739120e89dbb3ff045b3c8a8ff8864145bd35c0e7b8af7b843dbec52c`  
		Last Modified: Tue, 26 May 2026 23:15:37 GMT  
		Size: 20.2 KB (20240 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3c8c352918eef9d409afa910947e483fbe536792df77d6425fc799f88d73bcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116146222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d48ed56834b80a4f40f6c01918f9f289df3bc5758bad2ee460b1d77695448ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 15:50:54 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:50:54 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:50:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:50:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:50:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:50:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:50:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:50:54 GMT
ENV container oci
# Tue, 26 May 2026 15:50:55 GMT
COPY dir:a00d53b24bbcf9097132390b191c936ff622d9b440a8f192754b910ebb84f566 in /      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:50:55 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:50:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:48547272f4e6f96db66fd643aed1cfc9d3d7b7e696830a7dd166e3dd1a7a8aa4 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:48547272f4e6f96db66fd643aed1cfc9d3d7b7e696830a7dd166e3dd1a7a8aa4 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:50:55 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:50:26Z" "org.opencontainers.image.created"="2026-05-26T15:50:26Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:50:26Z
# Tue, 26 May 2026 23:08:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:27 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 26 May 2026 23:10:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:10:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6ba40b0a7d8c65538d55968f5725eca287bda3024401d2f12b225797f497e32b`  
		Last Modified: Tue, 26 May 2026 18:13:55 GMT  
		Size: 38.8 MB (38794791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7c900388efba22c6ceef84ace85c02597c24f0308bdf013bf3411429317d8`  
		Last Modified: Tue, 26 May 2026 23:08:59 GMT  
		Size: 27.7 MB (27693154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7ba6b1954f22d2cc0ebe7ba6164d7d94cb09a01d4c7f1d177f0d17dcc12d`  
		Last Modified: Tue, 26 May 2026 23:10:33 GMT  
		Size: 49.7 MB (49655860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75002aced0f32c0c87e07cd2c721b248f16fda5473b97db8cf8daadecd831e`  
		Last Modified: Tue, 26 May 2026 23:10:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac9794c0fda3533bf5e4e8409c95491e7833560ef62d7944dfd62ebe8a827a`  
		Last Modified: Tue, 26 May 2026 23:10:26 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f0c79a528715bed91c79c0a112e8b21702ffee78ff0dc69674a9531e36424e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b94d67a314ded0bd8344c563bc9066572acd28a4779b2c71a2d52d1b588b3f9`

```dockerfile
```

-	Layers:
	-	`sha256:a37950abb5909eb605c12212f706d7efb0b2af86bf9f0f1aa418aa174fb30b06`  
		Last Modified: Tue, 26 May 2026 23:10:32 GMT  
		Size: 2.4 MB (2403649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ccf6491a7c932504e82e0ebc8caeb2fab0b5b99f3c306e4417b37671071ba0e`  
		Last Modified: Tue, 26 May 2026 23:10:32 GMT  
		Size: 20.2 KB (20210 bytes)  
		MIME: application/vnd.in-toto+json
