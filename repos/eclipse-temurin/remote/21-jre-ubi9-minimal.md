## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:54ace8712221bbf4c3c75eec39496844c81d5d8e9f2575512b11c239b3e0783d
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
$ docker pull eclipse-temurin@sha256:e41203686c88cbe7e03fbb64fb48ae65298d0b196d5828ca6def06802e1f8965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123426156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e122a809532d7c31a562660c07ac136431597c0efe42d0a81d18d8f55b026c93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 00:41:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:41:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:41:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:41:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:41:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 02 Dec 2025 00:41:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Dec 2025 00:41:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:41:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:41:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886ff583b5cae0b313d0ef0bca871cfa47a18ef71182c90a8e55e9397c3c2c69`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 30.4 MB (30407401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a144fa28eab18fbc41b117adac519aca64aae122aa62f796c63a05b6ed6b0`  
		Last Modified: Tue, 02 Dec 2025 00:42:12 GMT  
		Size: 53.0 MB (52976256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e3679d6def24b3f0e49593486208f3583167992e31fb4e17c6e58b58bf95f3`  
		Last Modified: Tue, 02 Dec 2025 00:42:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b136d3a529bc2cb56cc0fbfefdbf886c1394f2a5de2bcd3bb13c9ae2ccc0b8c`  
		Last Modified: Tue, 02 Dec 2025 00:42:07 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ca48e2ab49e10f055f16a2f1d1a0ab32f2763ff1b7d8d8c65f4044379161cdf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2437010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab246667a6f27ea28fe25c1dc141e279fccd612f2d0cb04a363937d2460ee4f`

```dockerfile
```

-	Layers:
	-	`sha256:a9c8f9bbad3da257bac13a9305886b9a3f6c02a0e7604c8e04f73d1e3196b64a`  
		Last Modified: Tue, 02 Dec 2025 01:16:31 GMT  
		Size: 2.4 MB (2416825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51a2e4c402090e231852fdb826bbdca56416aa2979155f69f5be9ca8b356bb2c`  
		Last Modified: Tue, 02 Dec 2025 01:16:32 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8a74d2d1715f2ac67eb21ced9810c5ce4daa6ace697d6aad9eb99c78a54c6cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121218670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc04bef735ccedf1c596e23107912c6960e4b1f2232cfc25d93dc5ac2e57de37`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 00:47:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:47:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:47:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:47:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:47:23 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 02 Dec 2025 00:47:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Dec 2025 00:47:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:47:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:47:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488a06a33cb1fcd49b1e5ca4a60367e53447f921b2ab104546b2d18ac1569805`  
		Last Modified: Tue, 02 Dec 2025 00:47:50 GMT  
		Size: 30.9 MB (30853386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c73f11b71bf17937c25216b49d861d90c66bb2b862f76fc204e2fba30413705`  
		Last Modified: Tue, 02 Dec 2025 00:47:55 GMT  
		Size: 52.1 MB (52141158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f398de6bce2d54e8c2f6afa799f0f156a5d815f79f297189896abcb515e7c621`  
		Last Modified: Tue, 02 Dec 2025 00:47:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a106f968c57fa22e8455c911b66317d80fc3de83a4d25d7d1601fe25454ea4`  
		Last Modified: Tue, 02 Dec 2025 00:47:47 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d2d9fa911cf3aea927c39c7da242d680b2fbce465128aea019a35b450dc7d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd4af64e51088e4d36e9a05d2ab22da5f29edf37902f288039ebac0e0a0e237`

```dockerfile
```

-	Layers:
	-	`sha256:4295b40456e974f65be6caf80080865efd76d7237d7fe7ec2edba411566cee49`  
		Last Modified: Tue, 02 Dec 2025 01:16:36 GMT  
		Size: 2.4 MB (2416183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3417ca9f19f9e39701fe57a57c730a15993fc42bd8cf70193d721d5fb14d574c`  
		Last Modified: Tue, 02 Dec 2025 01:16:37 GMT  
		Size: 20.3 KB (20289 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:95f5344fd9cd9e675c29ee90508a7ba9c61b139a5b92c05bbc68518fc01209b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127535643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7388460d7f332a5193a0938d3d737f511de0979e6caaf6405e0ace45fe8a181`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:52:34 GMT
ENV container oci
# Mon, 17 Nov 2025 06:52:35 GMT
COPY dir:9a9add289f1055504c42bfa45e0dd9890598235dacbc2320fb6adf8f7795427f in /      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:52:35 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:df039a12e94c358b58fd977c386a5daf1a5d5ee9447df76db2fd5246917af6b7 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:df039a12e94c358b58fd977c386a5daf1a5d5ee9447df76db2fd5246917af6b7 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:52:36 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:52:24Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:18:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:18:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:18:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:18:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:18:50 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:30:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:30:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:30:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:30:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6fccaa32330f08c5e0cbe4fb16bd3e3944f9e113abfe46581e3f895ddfc1db49`  
		Last Modified: Mon, 17 Nov 2025 12:10:03 GMT  
		Size: 44.4 MB (44431008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ae5c71fee127db36920f76d71bcf3210a5ea9baf4a783f6ef553746a98cae7`  
		Last Modified: Mon, 17 Nov 2025 23:19:50 GMT  
		Size: 30.1 MB (30124462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e9ac67255651cd55deceff9be9ce3171a4d2671753262a7a9ce80ff0aba400`  
		Last Modified: Mon, 17 Nov 2025 23:31:15 GMT  
		Size: 53.0 MB (52977756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd98cca96a84f811a548560ba0b99440e0cb9fed253c7db755a906539b5e68c`  
		Last Modified: Mon, 17 Nov 2025 23:31:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f8f6082d9c74836d122e578b2fc7708359001dc1b7d702c26f22b7b1051e6a`  
		Last Modified: Mon, 17 Nov 2025 23:31:07 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:96c8beeb418b1b4414a03f61444d2521011f5a45fc87bfef026e85d2108d912f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a9f5b08a20fa11aa1d8e7babea60a4dc83683a968caf1ad25ba4e3b5d83ea8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc86bd739ffa7b63adf5c987ab38374099c88066ab5e6dd455c3d928313fb97`  
		Last Modified: Tue, 18 Nov 2025 01:17:42 GMT  
		Size: 2.4 MB (2407519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74c7070d325dc36d5d2c2065326000ba47cc8ff2136d4fffce31d35ff9763c4`  
		Last Modified: Tue, 18 Nov 2025 01:17:43 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:40d6ebe3be35caccdf8425fc6d42a7a5b61ffb82f66e46e174938f0a44bcb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118098693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25028246a53443f46a1a03876bd040fa4a87aeaaf7e1192812d7b4320bfbd18`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:55:28 GMT
ENV container oci
# Mon, 01 Dec 2025 08:55:29 GMT
COPY dir:fd64e83e16406d5844580a74bf276e335ef1e91b51af6932a1c38280460b502b in /      
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:55:29 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:b9982a341e331d0c55380d80e2a0ce568511a3c088f1b8a4ab833ee5de68d530 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:b9982a341e331d0c55380d80e2a0ce568511a3c088f1b8a4ab833ee5de68d530 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:55:29 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:54:26Z" "org.opencontainers.image.created"="2025-12-01T08:54:26Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:54:26Z
# Tue, 02 Dec 2025 00:33:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:33:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:33:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:33:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:33:28 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 02 Dec 2025 00:35:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Dec 2025 00:35:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:35:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:35:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c146ac3b9c14a1ecaff446a02862f803385ae46be28b17ca9bd879732615d0a0`  
		Last Modified: Mon, 01 Dec 2025 12:11:28 GMT  
		Size: 38.1 MB (38134676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9672b4ccf7dda7bee014c587130265e9d6ff2697b86542083325bac8f3102a0b`  
		Last Modified: Tue, 02 Dec 2025 01:04:50 GMT  
		Size: 30.4 MB (30445670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1506704179d37c976dcb2b199e39d1693754ea0986ab507ee433db881ee0ca19`  
		Last Modified: Tue, 02 Dec 2025 00:36:44 GMT  
		Size: 49.5 MB (49515929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1725231533f115b31b09f74a6efddeb44267a9a1600ca864f3df061375862b03`  
		Last Modified: Tue, 02 Dec 2025 00:36:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e46fa70e9c7929bf61a315f3edf72979cfd10fd231156a8e5e5bf53ff5c4cee`  
		Last Modified: Tue, 02 Dec 2025 00:36:38 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c62df6c11685322a69dce27b766075456cc4e7419d57b748258dc71b997b87ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2428803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93916ee4e1ff2f583afe273cdcf25ff256dc9b734f20d9347d715dd4daf7493`

```dockerfile
```

-	Layers:
	-	`sha256:c3e184b5a3e90885b3ed4ac78ade13c82cde1c5b5bdc54a6e34783e3871711db`  
		Last Modified: Tue, 02 Dec 2025 01:16:43 GMT  
		Size: 2.4 MB (2408617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7cc4b5966166322b9330e5d88ab57beb1695430c34d5d3a32a5f3950aa11a7`  
		Last Modified: Tue, 02 Dec 2025 01:16:44 GMT  
		Size: 20.2 KB (20186 bytes)  
		MIME: application/vnd.in-toto+json
