## `eclipse-temurin:21-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:7b68cc62221bd0add82312d6513e9e98d1e5b50339eb4221af99fce246f60461
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

### `eclipse-temurin:21-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4f918644016b6178feabb421bd52b71c7a8fb4435bfe4481aff6b72283a12c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247793535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999fbe4383d66a2ba929f0476794b24f51b04ad97dee4015d22d3b2f116bab6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 15:52:05 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 01 Dec 2025 15:52:05 GMT
ENV container oci
# Mon, 01 Dec 2025 15:52:05 GMT
COPY dir:e3f52ba99077b3bc7b7921467816c9e1d6afafe638b5c85f61d17a96c866d5a4 in /      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 15:52:06 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:922399bb1f6dd7741b16f1cdd9842f87612db7b462e38b1bbeae37d5c71e21d7 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 15:52:07 GMT
COPY file:922399bb1f6dd7741b16f1cdd9842f87612db7b462e38b1bbeae37d5c71e21d7 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 15:52:07 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-12-01T15:51:47Z" "org.opencontainers.image.created"="2025-12-01T15:51:47Z" "release"="1764604111"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68,org.opencontainers.image.created=2025-12-01T15:51:47Z
# Tue, 02 Dec 2025 00:37:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:37:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:37:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:37:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:37:44 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 02 Dec 2025 00:40:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:40:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:40:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:40:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:40:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3fe7185a3562260af267162d9816b8c41f88072fc86a6884c33d874ef0a74688`  
		Last Modified: Mon, 01 Dec 2025 18:12:29 GMT  
		Size: 34.6 MB (34621933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfd0be18fe4c33d84edfb20868c6ad1174990231e9a127a60cb06607ff7fab8`  
		Last Modified: Tue, 02 Dec 2025 01:02:53 GMT  
		Size: 55.3 MB (55340248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fb1eff9c9a2f72b6b0e285cb71fa945cb776769c5410c168ba0d9884da9703`  
		Last Modified: Tue, 02 Dec 2025 01:03:14 GMT  
		Size: 157.8 MB (157828935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71148002faea013301ab4f14e55c63d1585202a95d81514c3820e8de5033bfb`  
		Last Modified: Tue, 02 Dec 2025 00:41:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7009e9b22d4fa40642ea740a3ebfbf64ce6f1ee96f76a4d199d71f9f3608f425`  
		Last Modified: Tue, 02 Dec 2025 00:41:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8ffc8fffad3519576d40ca43dfbb33ac98245a964370972a1a9dfaec0da8f473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5704922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac56b383b7c1a8e15b1e7ce23be818cd696ce43c11df7fbac3f44d51f807014`

```dockerfile
```

-	Layers:
	-	`sha256:49ee2534fb48e7b7486daf2b01295bb4384e10bd3849bacbffc6bd0025db7327`  
		Last Modified: Tue, 02 Dec 2025 01:15:54 GMT  
		Size: 5.7 MB (5683606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1fdd85333dc2cb54860f5da7caf6b34c784c3535f0c6d80ce801d8788ce8c22`  
		Last Modified: Tue, 02 Dec 2025 01:15:55 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:75090b61034cf21a8b68fb3ba018c3218f2033274c9e2a265f6b435a58623578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243854922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3795324b56b24dd544fe66af5645f5deb1fd1d10c962fc75ded29b7d69d543`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 01 Dec 2025 16:14:10 GMT
ENV container oci
# Mon, 01 Dec 2025 16:14:11 GMT
COPY dir:69dd4a0b5ba0f5bf7a4e00ffeb7ef3c8fe0f0bfc2283402327c0309bf841d6fa in /      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 16:14:11 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:6f341067110dc29b8758b5d271970b09cd64dcb0e30a85b18012a177bb71753e in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:6f341067110dc29b8758b5d271970b09cd64dcb0e30a85b18012a177bb71753e in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:14:11 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-12-01T16:13:49Z" "org.opencontainers.image.created"="2025-12-01T16:13:49Z" "release"="1764604111"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68,org.opencontainers.image.created=2025-12-01T16:13:49Z
# Tue, 02 Dec 2025 00:46:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:46:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:46:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:46:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:46:06 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 02 Dec 2025 00:46:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:46:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:46:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:46:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:46:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c27140b3e778c26a038c982eb0b0d7c55918358b1c1e3afdb013d53d318ad1f`  
		Last Modified: Mon, 01 Dec 2025 18:12:35 GMT  
		Size: 32.6 MB (32592499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8142de3dd1b1e18b8b67f377d2e3c4667a1dc23363c391e1c1c877ca053fb3`  
		Last Modified: Tue, 02 Dec 2025 00:46:51 GMT  
		Size: 55.1 MB (55148145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797b3dca72003246bf490eda5acd294c1e9701ff53a41c30a20b24c0d9163719`  
		Last Modified: Tue, 02 Dec 2025 00:46:39 GMT  
		Size: 156.1 MB (156111857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feef781ccbb1ea4a01e5231f85e97ffb76ec25e96ae11b5d1070671655be4062`  
		Last Modified: Tue, 02 Dec 2025 00:46:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0115ff700d8a146432d832295d6116db568de5222db9cf24fd84bbe93806b2`  
		Last Modified: Tue, 02 Dec 2025 00:46:36 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e5c29c8cbb239923b9c7683c9be2b02982454d69a4ca408308ff1aceedb66d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5704528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb92d7c860e839a1cc18caa876d588e8cb8a1c84502a2cf13d88a9c7693eabc8`

```dockerfile
```

-	Layers:
	-	`sha256:6c0e4944ae96c80ef3b415f577a07ed4027406afe17d66443926684907439a10`  
		Last Modified: Tue, 02 Dec 2025 01:16:01 GMT  
		Size: 5.7 MB (5683096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2e561be50191a96bf83dbd2311622ac5f83c999ce2d48e87522944caeea1142`  
		Last Modified: Tue, 02 Dec 2025 01:16:02 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:962bccd3636d870020f7a19ef4c82078d2eebb9c089da2cdffcd134e19aa627e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254021056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f24e16a2db32987f856f9b8e39ed7eedd2146c2465c0f738c528e64fdafc1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 17 Nov 2025 07:03:31 GMT
ENV container oci
# Mon, 17 Nov 2025 07:03:32 GMT
COPY dir:3f836289fcb5e4834914ff52d15c42d6b925906d318eaeb6e7ece83b813f7798 in /      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 07:03:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:040b4789124c20d56e0f81f37d756e271408963b29b2b4b1e2a7e2c073e4ad50 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:040b4789124c20d56e0f81f37d756e271408963b29b2b4b1e2a7e2c073e4ad50 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:03:33 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-11-17T07:03:20Z" "release"="1763362715"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:49 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:27:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:27:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:28:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:28:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:28:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e24e81139d30a463716e63229e1184a2b4250bb139ff88e3682c9e552661b81`  
		Last Modified: Mon, 17 Nov 2025 12:13:13 GMT  
		Size: 38.7 MB (38721761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106e259b55af997c3f2efc1cf8633c914cd06061615b03cbef4967d4541d920a`  
		Last Modified: Mon, 17 Nov 2025 23:16:28 GMT  
		Size: 57.4 MB (57353400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b47d688600dfaa21919a222421ab533fd76f3320b1d25aaffefea5b7c98e45`  
		Last Modified: Tue, 18 Nov 2025 01:39:17 GMT  
		Size: 157.9 MB (157943477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a2d9c0e30ec72903f3bc48a6157f226336541d959c03807a7e9293ebbfdead`  
		Last Modified: Mon, 17 Nov 2025 23:28:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5be7a9d8c4fd0f8e8f151417d5292dc9e5de9ba06e3bd48c1f85d8d9521018`  
		Last Modified: Mon, 17 Nov 2025 23:28:57 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0747d081bbd3075dda5c61c56623abc7c034373d550eeaf13231af822cc107bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c764b317403df730a4009dc512118b62dd43f2b7310549f31b44ae2838031b`

```dockerfile
```

-	Layers:
	-	`sha256:b8453ed83dec77e8426762bd2dc71e4155c0a6abd21bc9f135ae129a4bb55b73`  
		Last Modified: Tue, 18 Nov 2025 01:17:00 GMT  
		Size: 5.7 MB (5670758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434ace1a048e9972bf84d95f49b111d64ae7888e0e40a5f2340b97c4243bb63e`  
		Last Modified: Tue, 18 Nov 2025 01:17:01 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:da4f834c7165273b8dfea402f8417c99a5187484914d18c92e3747774d75d356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237380845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e49024b5b5df3c899c83ad44da1aa4f7f515deeb3c2aace123bb8b5971dd44b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 01 Dec 2025 16:13:45 GMT
ENV container oci
# Mon, 01 Dec 2025 16:13:46 GMT
COPY dir:ee1f1fb58b73712e067b524f29b07cf434abeebd65fa952bf194a31a9e96dd28 in /      
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 16:13:46 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:178efaed95a9f3c67a11443e55f39f4bf9d142ac34782d99fc4d745647dcdc7b in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:178efaed95a9f3c67a11443e55f39f4bf9d142ac34782d99fc4d745647dcdc7b in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:13:46 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-12-01T16:11:22Z" "org.opencontainers.image.created"="2025-12-01T16:11:22Z" "release"="1764604111"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68,org.opencontainers.image.created=2025-12-01T16:11:22Z
# Tue, 02 Dec 2025 00:33:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:33:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:33:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:33:30 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:33:30 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 02 Dec 2025 00:35:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:35:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:35:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:35:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4c2d3b17031accf5277814f24c5959875fea29c3417bd21d9ab38a4021f9b098`  
		Last Modified: Mon, 01 Dec 2025 18:12:30 GMT  
		Size: 34.4 MB (34366787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d6f29237cb9bac260bb875e3ab78f2c39de4f6195073d574380d496293d5d9`  
		Last Modified: Tue, 02 Dec 2025 00:34:52 GMT  
		Size: 55.9 MB (55943138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fcffc842c50a02ecf693cc3cb57746af4586245f8dc5cfc4063628854ac8c2`  
		Last Modified: Tue, 02 Dec 2025 01:02:45 GMT  
		Size: 147.1 MB (147068498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9c415ad2d9e5ac359512d2f0cc6ec214355d4ab5cf8494a2cb90a0c0fdf09e`  
		Last Modified: Tue, 02 Dec 2025 00:36:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c75eddf9a42a7c74ecce84d23f99254cff85f38878bf0dfbf28b6c6ba38363`  
		Last Modified: Tue, 02 Dec 2025 00:36:58 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5254507e3252d2285c3cdc9a35f81b24bceb6d6588f7a92218f7a26bb23ada90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5690447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a737b17f1eae224e793eb25ebb72df7ad948b78a440061532b72928abb546e1f`

```dockerfile
```

-	Layers:
	-	`sha256:3490cdaf3a45db52f5096cd1eaa9f4b1c3c2088fd0d58e49ce7b49b53a31884b`  
		Last Modified: Tue, 02 Dec 2025 01:16:11 GMT  
		Size: 5.7 MB (5669132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a784395773809d6f79319a1cb163521d9c4175436cf38ec9d4cced8b5a563378`  
		Last Modified: Tue, 02 Dec 2025 01:16:12 GMT  
		Size: 21.3 KB (21315 bytes)  
		MIME: application/vnd.in-toto+json
