## `eclipse-temurin:21-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:f349bf14fe2666b8e5b78d7507ef34c806455e58123e621b6baa4d8b18d4a5be
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

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:85d104a8da6d16a9d248574c8b1c3263880a326b04ff61feb29c242c1fec3acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252132561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecbc6eec66ca94290e421569621eb4419bff8abbdf3c2f241e97beb384eb04b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:00:41 GMT
ENV container oci
# Mon, 10 Nov 2025 09:00:41 GMT
COPY dir:1151487a8fe49bf6a88ef514a8355cedfdeab84f41175ca19d399c25d56e0756 in /      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:00:41 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:78d340a91825c21b9da1409e53e49b8dfe282306bad9ddfd7c9094f83382378e in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:78d340a91825c21b9da1409e53e49b8dfe282306bad9ddfd7c9094f83382378e in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:00:42 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:00:19Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 20:10:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:10:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:10:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:10:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:10:52 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 10 Nov 2025 20:10:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 20:11:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:11:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:11:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 20:11:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32b34b6043df53356073fca74558aa4fb64fa2c3d92bc988ada13ba9600db416`  
		Last Modified: Mon, 10 Nov 2025 12:11:59 GMT  
		Size: 33.4 MB (33442309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c735f78a5f1b6620ea84cadb59081812182b4d06d9bd1b87186428ddcf35083`  
		Last Modified: Mon, 10 Nov 2025 20:11:35 GMT  
		Size: 60.9 MB (60858887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f4e419bd555714a77a33dc132d5b6fad5995725319b11e00f3a6145ffa771a`  
		Last Modified: Mon, 10 Nov 2025 22:30:37 GMT  
		Size: 157.8 MB (157828944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27213255f2051fc0e908b21ff013f86fc1626dedc9e5562da4e9ed353a5ac82a`  
		Last Modified: Mon, 10 Nov 2025 20:11:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e38bdf526f86bf415d97442d2da1493c0d43c4c30a0aa023b1e16295d6fb2d8`  
		Last Modified: Mon, 10 Nov 2025 20:11:27 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:650a5340b49d2301a2162db821e9267d0f6109e629eb4baafa845cdf564911fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5698958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a65691c5488ee53b44d888aba0e8e9c74ed88f852b9bbc63d3a08e400d4a57f`

```dockerfile
```

-	Layers:
	-	`sha256:c03305fb252316818ba28487d0a123ec9626b22ce3ee6a1c185d0a9d57bf9d50`  
		Last Modified: Mon, 10 Nov 2025 22:14:36 GMT  
		Size: 5.7 MB (5677642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75223ffe75c1758ff7f4ec59284dcfafc24627093a56ebee7219cc3402d52de1`  
		Last Modified: Mon, 10 Nov 2025 22:14:37 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c76cef34879c9b6367af78d384fa0dfd5d0b67e404ae19db9a4d4886069a6708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247575895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa60e287d8060b36a72977bce2665511233d4e3a624283e5c68c5e82bf15a7b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:03:37 GMT
ENV container oci
# Mon, 10 Nov 2025 09:03:38 GMT
COPY dir:5f27c3cb719e482fe521704b0fcfe8823184f7bac7981ef4facb5aa58eacca9f in /      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:03:38 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:b708d1caa910d276ff58faaae8986ef542efb0b7b3e35c86e7086c7765f4ff1a in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:b708d1caa910d276ff58faaae8986ef542efb0b7b3e35c86e7086c7765f4ff1a in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:03:39 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:03:16Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 20:15:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:15:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:15:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:15:04 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 10 Nov 2025 20:15:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 20:15:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:15:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:15:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 20:15:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bcfce2f653765e7fbc0157676a8995e7c79e4d29c562744818763bd665844191`  
		Last Modified: Mon, 10 Nov 2025 12:11:55 GMT  
		Size: 31.6 MB (31555554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec07ce9a6924091bd5fa52212029fff0875a3d34bcfdcf6424b1c07ffa22f27`  
		Last Modified: Mon, 10 Nov 2025 20:15:49 GMT  
		Size: 59.9 MB (59906103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71b9ff826c109df9adc513a9e0065db89680d5d314d1bf18111ad9dab5eede6`  
		Last Modified: Mon, 10 Nov 2025 23:14:57 GMT  
		Size: 156.1 MB (156111818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b997064ab20516897aea25449f4166d48233585484c2c1ad3c25ff06ebd9bb2`  
		Last Modified: Mon, 10 Nov 2025 20:15:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ba95045c33aad72844121ea768b05682c63ff44ff23cca93cc02a9d8d8bcb3`  
		Last Modified: Mon, 10 Nov 2025 20:15:44 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b80b5924266dd1983a51c773663b136bb93555dd66de9094dd981aaf60a9c1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5698564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1d98ff28f814adc0dd5060f959e69a7cf4bf4039928d25904d0ec038042f25`

```dockerfile
```

-	Layers:
	-	`sha256:112df9c7264be210c5b7e013095bfa2d52001529ee4d3722b92c21596e9d9125`  
		Last Modified: Mon, 10 Nov 2025 22:14:42 GMT  
		Size: 5.7 MB (5677132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d351618b8a0a14c0f08c7403c1d8a57acc7c163902984bbed8e525b4669b1b09`  
		Last Modified: Mon, 10 Nov 2025 22:14:43 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b485ce7af620b939ed69009e0fd6af90769b9ec415bc6d582c723e52e1e36cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259041719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19cf747c295cd7153459dfa318d6807a33b1cf57c2ac9cc6c927abf62fa129e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:07:33 GMT
ENV container oci
# Mon, 10 Nov 2025 09:07:33 GMT
COPY dir:3b3b10e38b1604be9ad4399ace6288103b3f832d58ec15ea17ba00ea93e2b9f7 in /      
# Mon, 10 Nov 2025 09:07:33 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:07:33 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:07:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:c064500eaa9793e932d2f4ef045195d7141f0508959d80bc76c0e4b59b13a481 in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:c064500eaa9793e932d2f4ef045195d7141f0508959d80bc76c0e4b59b13a481 in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:07:34 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:07:22Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 22:20:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 22:20:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 22:20:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 22:20:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 22:20:01 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 10 Nov 2025 22:25:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 22:26:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 22:26:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 22:26:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 22:26:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4228be713e86c1bedeefae4a08794664efeed4203b55a759503d7eaba4964702`  
		Last Modified: Mon, 10 Nov 2025 12:12:00 GMT  
		Size: 36.8 MB (36758319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c50dcfec7b2b334fc4e91aecba50a60520f8dc961a0ec542db5fcf328613c`  
		Last Modified: Mon, 10 Nov 2025 22:21:05 GMT  
		Size: 64.3 MB (64337609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa547e448726e7a9febba5cc9e515d34905aad5911ef24cc88da387d7cf84e1`  
		Last Modified: Mon, 10 Nov 2025 22:26:46 GMT  
		Size: 157.9 MB (157943373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad831235172f99315dbe33cf4b89ac65f853b90a68321787f763c454386cb91`  
		Last Modified: Mon, 10 Nov 2025 22:26:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d037b495a10e2340c034f884a33611a92625355697457990ec6c0382ec63c5c6`  
		Last Modified: Mon, 10 Nov 2025 22:26:51 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:45ee8f4ce888838f7d5b1943484005a12d37a387e00df09dab966c01e924f07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8438d438e34d1d620b3dfe5eb32c30216a2a4ab05120e5aab7117aaa048119f0`

```dockerfile
```

-	Layers:
	-	`sha256:6a6359b3a1532a8911ed4c939a91b4605e45e64bb3226fc81c48ea1654bbc49b`  
		Last Modified: Tue, 11 Nov 2025 01:14:14 GMT  
		Size: 5.7 MB (5664794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ea2cdee90173c444c691327fb5561e810911b3f541262c51d33c7b53255887`  
		Last Modified: Tue, 11 Nov 2025 01:14:15 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:5f632c4876970d81167018d89b84ebe949f14e9257c23f84577b621846e1f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241409156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec598f14fd704c0f274265848b45171f737c5cb9c1ed14952d0d61a81c4de7fd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:29:45 GMT
ENV container oci
# Mon, 10 Nov 2025 09:29:46 GMT
COPY dir:6c57839ff9e4376687d005b2dd39ccb2cab51f91439029283a68660066f453ce in /      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:29:46 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:e7aca2e85df2b708be29fcf6492e0a97a7c66021e1c9892fbb96b00e6743eb74 in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:29:47 GMT
COPY file:e7aca2e85df2b708be29fcf6492e0a97a7c66021e1c9892fbb96b00e6743eb74 in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:29:47 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:27:31Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 21:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 21:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:51:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 21:51:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 21:51:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 10 Nov 2025 21:55:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 21:55:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 21:55:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 21:55:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 21:55:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7f1c5bcca4741d297e22f1dc3025949ada86e7918c015239fbbf81971759082f`  
		Last Modified: Mon, 10 Nov 2025 12:11:54 GMT  
		Size: 33.4 MB (33403080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753a4bd28d57ae0089cf8c05a2fbb3b40711d6fae82766de9b160ebe59e240fb`  
		Last Modified: Mon, 10 Nov 2025 21:52:19 GMT  
		Size: 60.9 MB (60935183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291e767e596040e8e0e0943e7f808e8e30f1fcb19dab3192c37ec7da9cbef3f`  
		Last Modified: Mon, 10 Nov 2025 21:55:48 GMT  
		Size: 147.1 MB (147068473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd6fad2270b98cf983462fffd9c1a270f32b51d8eff9d546699607a3c00c372`  
		Last Modified: Mon, 10 Nov 2025 21:55:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bacd65de884650f71a990929ee3e7fbb2e65d14b84acb35adb7af9e15de0e`  
		Last Modified: Mon, 10 Nov 2025 21:55:54 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e2621d7e1659b270ef2655daafbedcb124fd20742cdeea730d0fca688e48c595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5684484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9533c6ac0f5e7b289176e0df41567492875e4aed7fed8bddcbf857f1350c72`

```dockerfile
```

-	Layers:
	-	`sha256:0a9b2db1775dd371a63ddba28b77b6f6d5f4080f3e69aa6bc93bf62d7a2dc8bb`  
		Last Modified: Mon, 10 Nov 2025 22:14:53 GMT  
		Size: 5.7 MB (5663168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f964a87cbb29aef4952508c236a493dc6b4e5f5da1a00fecf96b5500ab2920d`  
		Last Modified: Mon, 10 Nov 2025 22:14:54 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
