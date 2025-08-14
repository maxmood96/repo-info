## `eclipse-temurin:11-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:91732926721d952bac92d67c157990bcb525ca6a617654ea883bb8f1c3ce167b
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

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9eec704bd29231087faecf657b95864e2a8b1a3c22365f03221230321f1b9cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132831786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858e6d2a289ff103c99308c4e0c88647663840b2bb1fa70f0f1f3204203bdf9a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:fe33f3d694b6e20455a988c4bdb920e5a216d54c81a4c79494b6d0debd58f76f`  
		Last Modified: Fri, 08 Aug 2025 00:12:36 GMT  
		Size: 33.5 MB (33498072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09cb14241db0085c2bc2c6b59f3cf7beb9fe096ebf7637bfbff9cd6baadbf77`  
		Last Modified: Wed, 13 Aug 2025 23:02:04 GMT  
		Size: 55.1 MB (55090775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5b1fff1ae100f1ef44515c06b23342a9a8c01bd002e6a21ff426422ece263d`  
		Last Modified: Wed, 13 Aug 2025 23:02:18 GMT  
		Size: 44.2 MB (44240520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d960f9f74db25007cbbae2d10ef169fca9fecbfb41014e19c634c0907be842ad`  
		Last Modified: Wed, 13 Aug 2025 23:01:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d03a124bd2882adbb315beda65e72bf117ddb614595469de9ea96b88eab2a5d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c6ddcb779459fa33dd26c054fc6a33c5dca41998e6f564e24e66905853f52285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5622352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5325c6384e636eed47c0ad27813984816cdaebc519534d325074dd0150a47b50`

```dockerfile
```

-	Layers:
	-	`sha256:a0babdeab1b1aa8b360f8f43983d9f1f66874dbede38a210a65f52c0c9d5bcbe`  
		Last Modified: Thu, 14 Aug 2025 00:12:47 GMT  
		Size: 5.6 MB (5601955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744dbee89ae4804d52eda09e09cb438c42d30bd25e062dd27cd242716c512504`  
		Last Modified: Thu, 14 Aug 2025 00:12:48 GMT  
		Size: 20.4 KB (20397 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:685b56dc7a4ca663058f2d0a1d3156fe8725c6086215c61520259ba928bd20b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129012072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582eb9795eddcdabdf3e0707a2a097f3686e3794e750d963d531786e23d5ced0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:95bf6781bf0810cd2cbd6677a3af273c2399a2f5ed0cb746f6fcab343c155799`  
		Last Modified: Thu, 14 Aug 2025 09:11:52 GMT  
		Size: 42.6 MB (42600500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eec643445b61896955f55fa506b70e52ea36ae7198e0da9e9dabf75c7e698d`  
		Last Modified: Thu, 14 Aug 2025 10:03:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83d9bafcf87cf8d26ee92534457e8562763ea5b5e0818fb1d758bc09b389026`  
		Last Modified: Thu, 14 Aug 2025 10:03:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f3d4e43154022337ff75e8107d7496897bea2dd376b23e4ff7584ff9d3e10715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5622552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da7c2caa05c3dbc2c03c31a517c133a3b5cf6b804b6b4a71f39d758829c96a3`

```dockerfile
```

-	Layers:
	-	`sha256:ca600ffe20d910415684ccf8f4b068a337eff4a6c740b26ed3b61405ab70dd92`  
		Last Modified: Thu, 14 Aug 2025 12:12:50 GMT  
		Size: 5.6 MB (5602051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7585b37e03df42e9d6f123482a98bc50b9daa8076e219ce79ac2c3a9b5ce4d1`  
		Last Modified: Thu, 14 Aug 2025 12:12:51 GMT  
		Size: 20.5 KB (20501 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e8318314e0e7e304f9a63203f1b5872cee190e7d18a0c90658cc082e24cc8983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133644373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83912cab096875cc638d736cb7d3fc25ead14ebb7f86f520472cd2583d1a5d71`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:db1ea3fd8e911786a6701733346cf93592a7e9ae4f51e225b206c4ddaba09f92`  
		Last Modified: Thu, 14 Aug 2025 04:51:33 GMT  
		Size: 39.7 MB (39731569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37649a332ad38fd02b7090010d262c2d77364671f3927e0fd50156d00f17b810`  
		Last Modified: Thu, 14 Aug 2025 04:51:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fa6b90e208f9c5dd9eff65ca178f9c2a4edacce77f7f938b520af4290f7dd4`  
		Last Modified: Thu, 14 Aug 2025 04:51:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a35bd9eebb17f1ff5fa2343fb752bb31a28bdb40b80799e47a8a910c7a479a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e579207a1b7affdf09867713f919d3cf0b53c18a75632714167222a7a3426a`

```dockerfile
```

-	Layers:
	-	`sha256:5a65e3193b646f79424b63ea86794256e82f6901037fa3e0d0af1c54ea1e3429`  
		Last Modified: Thu, 14 Aug 2025 06:12:59 GMT  
		Size: 5.6 MB (5591026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ebcc2f2486d08a53e451057d5f5868181f9e8a764af18119b9b3662be98828`  
		Last Modified: Thu, 14 Aug 2025 06:13:00 GMT  
		Size: 20.4 KB (20427 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:0cc8dcdbcff38a556de2501ccd1ca62cd2cae8fd64ebecf2d592a6da94d29632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126908009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7134cd8290ff65b7207064b0c30714d88da9c9b2eb2620ed781280a38077f3b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:5a10cba2d25371bf9396c9e436d4c27a616979a8b243531d1bb7b3daeeec536c`  
		Last Modified: Thu, 14 Aug 2025 04:01:31 GMT  
		Size: 37.8 MB (37820144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3bbcedd9775cf5844773c59704e602eaacc33d890f617f1449b97646858503`  
		Last Modified: Thu, 14 Aug 2025 04:01:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3c0224c57fba287fa3e263f5cdf985e941ae1b440d53619731e87f8f60d70`  
		Last Modified: Thu, 14 Aug 2025 04:01:28 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:34897d2d65fd2905f8acdd29d2497a7f4fd62c9d0b3619724edc9eaf2051f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ee975c1686e037c70275478f2e9da6538873e1f7416fde646869cda6ccd455`

```dockerfile
```

-	Layers:
	-	`sha256:496346a45b6d3414bac987575a8185d9516bf0fc7de92ecbd6f0fe734db778b9`  
		Last Modified: Thu, 14 Aug 2025 06:13:05 GMT  
		Size: 5.6 MB (5591887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4bf0c4ef2ea5d9b7bc0dd9d20592e7ef2fec46dd84fa17e6aa4d7e3e7ea2656`  
		Last Modified: Thu, 14 Aug 2025 06:13:05 GMT  
		Size: 20.4 KB (20397 bytes)  
		MIME: application/vnd.in-toto+json
