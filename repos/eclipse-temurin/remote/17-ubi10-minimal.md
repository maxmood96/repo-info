## `eclipse-temurin:17-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:a5f51018aed1a6b607fb0361505330a2c3c4a08156668cf194857d80db71c02f
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

### `eclipse-temurin:17-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:504dc38f657e7b1f81e377c8ad0cc9e638ea576e1d0cea9c4913c03cd0913251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219629256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5774b306ebcd7c5fae672477007b190c26ed2735af94f59db52b012d0f459f5a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 13:43:39 GMT
ENV container oci
# Tue, 27 Jan 2026 13:43:40 GMT
COPY dir:c206a7c74c2764db52e4fe9e9bb5506227dd2a550e47afa696c9a7c923f9a0ff in /      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 13:43:40 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:8db1dc4b84412d8a3137b92a8b51dc81382218dadd1dc925bd2c056986c8eb72 in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:8db1dc4b84412d8a3137b92a8b51dc81382218dadd1dc925bd2c056986c8eb72 in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 13:43:40 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T13:43:17Z" "org.opencontainers.image.created"="2026-01-27T13:43:17Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T13:43:17Z
# Wed, 28 Jan 2026 19:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 19:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 19:00:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 19:00:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 19:00:39 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 19:02:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 19:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 19:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 19:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 19:02:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6af7d70117fb54a1c19fa7ab0dd6387be5ab897497b2986acffbb49ebe56b290`  
		Last Modified: Tue, 27 Jan 2026 17:15:27 GMT  
		Size: 34.6 MB (34556452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f43f89163703a5ad210893837e14e26c900f728b405f5ed19d147e9b95d5e`  
		Last Modified: Wed, 28 Jan 2026 19:01:05 GMT  
		Size: 40.2 MB (40217468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb0d388fc6dc6930c5b2177556ecf431de3b27fa877520f7d4d7286f29d1a62`  
		Last Modified: Wed, 28 Jan 2026 19:02:28 GMT  
		Size: 144.9 MB (144852914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d9557bf5b04cd44b2f483f233a47eb64493cc1eabd81eea03a00864a805964`  
		Last Modified: Wed, 28 Jan 2026 19:02:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139047cc2817fe6386b34eba58e67691f5c2d576b02b40239a7a4b049c8073e3`  
		Last Modified: Wed, 28 Jan 2026 19:02:24 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7a6b03f9b2549ff179f9bf1289676ab03e1a3ae00bf6e02fae9cd3374dce52b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa414e971eefd5e670e4d0362cb4639ff0970962702961a76790a6ad62779ac`

```dockerfile
```

-	Layers:
	-	`sha256:b53ec259ad43c2a588416bb596499ee62a75d6536bef2749df4be2104461fb9a`  
		Last Modified: Wed, 28 Jan 2026 19:02:25 GMT  
		Size: 3.8 MB (3788457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c00d50afb5f1071c03033b287bdfde0f527f6ffd89717ef7b57f40bc16e18d6`  
		Last Modified: Wed, 28 Jan 2026 19:02:24 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2c4428f69c4bc9803e62053564c5d5c7de57924fd73626b1665ed0ee72b1eb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216268117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3f2834e6b9a3f3e08491f4bfab31c758fdb7fa43092a610b3806ba6f80f1ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Jan 2026 13:47:22 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 13:47:22 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 13:47:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 13:47:22 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 13:47:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 13:47:22 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 13:47:22 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 13:47:22 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 13:47:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 13:47:23 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 13:47:23 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 13:47:23 GMT
ENV container oci
# Tue, 27 Jan 2026 13:47:23 GMT
COPY dir:dded715b3a0a2e164f20d3adb11022b8895c6c71441752b542efe8b308cfdf47 in /      
# Tue, 27 Jan 2026 13:47:23 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 13:47:23 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 13:47:24 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 13:47:24 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 13:47:24 GMT
COPY file:5e2c60878f4f5d8054b61f4e5098ea8146de59bdabb4f983a6e2dc4f8443e452 in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 13:47:24 GMT
COPY file:5e2c60878f4f5d8054b61f4e5098ea8146de59bdabb4f983a6e2dc4f8443e452 in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 13:47:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T13:47:02Z" "org.opencontainers.image.created"="2026-01-27T13:47:02Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T13:47:02Z
# Wed, 28 Jan 2026 19:16:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 19:16:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 19:16:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 19:16:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 19:16:27 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 19:18:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 19:18:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 19:18:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 19:18:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 19:18:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c6ded6228935d623c0f495201219b24e5b514c514c166c86c99fd8747f446a4`  
		Last Modified: Tue, 27 Jan 2026 18:12:15 GMT  
		Size: 32.6 MB (32617493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827f43c619cd65bcc83a926309bae530896e6730073bbf06542d67407e6ad975`  
		Last Modified: Wed, 28 Jan 2026 19:16:48 GMT  
		Size: 40.0 MB (39962806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725b248f9679524afac3c28c0584e3017fcfcc88433c1170c23e48f43357718b`  
		Last Modified: Wed, 28 Jan 2026 19:18:49 GMT  
		Size: 143.7 MB (143685397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03a8606a0b1207cd2bcd07cb5f4b36c6f41b7b2b98332e23ed0323ac24e60d3`  
		Last Modified: Wed, 28 Jan 2026 19:18:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5f637cced1b6c230f2913622b834f601409c4470f20d8435502f8ea150f545`  
		Last Modified: Wed, 28 Jan 2026 19:18:45 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5ceae5ad339ab6cf19f3d780474eaeee279d326bd97959007fc9a1f3c265a0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2030c6c40713fabd77555d677d9dd5f99c797c09121e9c22d8cd7d1b93b5af`

```dockerfile
```

-	Layers:
	-	`sha256:35988392f103f04aa47cbd896c4abfdb6630bf6ed1d7512de864cbe87dd52e97`  
		Last Modified: Wed, 28 Jan 2026 19:18:45 GMT  
		Size: 3.8 MB (3787883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74e15d0e109fcfa44862562fbb330696ce8d0c722e450b321800893f58feea8`  
		Last Modified: Wed, 28 Jan 2026 19:18:45 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:66ece531363ab1595d9b92b48133b50ec07c513a100a03bb30bc522d0f0b4a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222315365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6f690c6c30648b7e9011b2459bca458e47ca085c315558e4304a5e6b2c79d2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 15:50:35 GMT
ENV container oci
# Tue, 27 Jan 2026 15:50:36 GMT
COPY dir:b1fb54cba477aa8e5cc12c75f143c33f00068a49e572e2a9058ca695db013356 in /      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 15:50:36 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:7b0b7973b756ae5fa48a994ea290e7e8ecbd19057a845071702a88d3f44c82d7 in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:7b0b7973b756ae5fa48a994ea290e7e8ecbd19057a845071702a88d3f44c82d7 in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 15:50:36 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T15:50:23Z" "org.opencontainers.image.created"="2026-01-27T15:50:23Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T15:50:23Z
# Wed, 28 Jan 2026 18:56:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:56:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:56:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 18:56:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 18:56:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 18:59:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 18:59:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 18:59:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 18:59:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 18:59:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ae80e80c08d44fa3239f0258ba6b08c404cdebc7b53393a151fa1f93bcf7bf6e`  
		Last Modified: Tue, 27 Jan 2026 18:12:32 GMT  
		Size: 38.6 MB (38638820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3882d9c01ea5c0cb5dd62cb2df6f92c42b9844d566e2f851eefbf5dc55868c`  
		Last Modified: Wed, 28 Jan 2026 18:57:36 GMT  
		Size: 39.1 MB (39126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231fc6203effda1065a6fa4ce1bb1ba0185b01b48ea4959c431e624a811c651a`  
		Last Modified: Wed, 28 Jan 2026 18:59:44 GMT  
		Size: 144.5 MB (144547869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c395ce07ba9728c11a191deb3e8600aea74cf0ea5736b334fb5ead1af02cafa1`  
		Last Modified: Wed, 28 Jan 2026 18:59:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c59c9c138ffb0cb498dad8acd3dc43eedcfcc364cc192da3e30344137c5251`  
		Last Modified: Wed, 28 Jan 2026 18:59:41 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:545a61b4a178b5753fc182ab0edaad3acd8a91605812402368be3b00ff71ad77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f303cad7d4b1bc487840b2c1372f049ef6046ebd3233862776dca0dd1da7cc1b`

```dockerfile
```

-	Layers:
	-	`sha256:2d49a32a612cdf38fe4c8130041324571fd21c801a0354a22eb1775a2ad1e7eb`  
		Last Modified: Wed, 28 Jan 2026 18:59:41 GMT  
		Size: 3.8 MB (3775289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9b737ac066cedab1557dc5c5832c2da5d62a04ebc3208ac3911c493b5601ee5`  
		Last Modified: Wed, 28 Jan 2026 18:59:41 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:788d1b3f52a4521f4fb60ff3903fefebce6bdd435d8f58cb50aa9b56deb58e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209601365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632715547bcd662865efd9dc23a1daf779afd28376ff4c0401138ed778cd067c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 16:00:26 GMT
ENV container oci
# Tue, 27 Jan 2026 16:00:27 GMT
COPY dir:4f1adb6a08f1772cc4a3a6f7fb169c42da3905eda1382dfd020cde9bf8ce54ed in /      
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 16:00:27 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:7d6813f56262fe28e046f6d0aae045479ae2fad09337cb7cdde0415772e612fe in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:7d6813f56262fe28e046f6d0aae045479ae2fad09337cb7cdde0415772e612fe in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 16:00:27 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T15:58:08Z" "org.opencontainers.image.created"="2026-01-27T15:58:08Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T15:58:08Z
# Wed, 28 Jan 2026 18:57:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:57:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:57:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 18:57:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 18:57:03 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 18:57:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 18:57:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 18:57:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 18:57:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 18:57:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d64b2731e63f62ba158833fc228878293975e79a79748090a59385ed70b4508`  
		Last Modified: Tue, 27 Jan 2026 18:12:24 GMT  
		Size: 34.4 MB (34372082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec036fcfe60084971e44fdfa9e8e4d4958b862be6f2c627225ff2410685c3ba`  
		Last Modified: Wed, 28 Jan 2026 18:57:29 GMT  
		Size: 40.4 MB (40364641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f3ba349f9b530ffbb309fdddbb3ab013d69fd9840f7aa32d3cbf21ed4bb992`  
		Last Modified: Wed, 28 Jan 2026 18:57:37 GMT  
		Size: 134.9 MB (134862221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577fce09232de2d936abd5d58d33915bde6b09c8ce76ca03d422414ab328ed7b`  
		Last Modified: Wed, 28 Jan 2026 18:57:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b52aa4e4b6fb504fceeff1bfe12977df204e6a192a202e7950810f3c69b39`  
		Last Modified: Wed, 28 Jan 2026 18:57:34 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:775e4fada79a0099c3e8e81c012fea94e8ac81dcbe4bad1c9d06da98a29d3bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3fd449f35a5be4377f67590ab668c544203dfc099a2774f0734b785caad6a0`

```dockerfile
```

-	Layers:
	-	`sha256:91ef9282e8e52c615991fe9b8d7453dcdfa53dae7dadff63da000c0eed0d320b`  
		Last Modified: Wed, 28 Jan 2026 18:57:34 GMT  
		Size: 3.8 MB (3774047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfaa83f9c8ba8c1ed1df53092190767e08a705db7cba27d09a4d7ab97fb85c8e`  
		Last Modified: Wed, 28 Jan 2026 18:57:34 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
