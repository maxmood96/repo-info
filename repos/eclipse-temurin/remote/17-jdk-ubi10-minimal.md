## `eclipse-temurin:17-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:ff968363f5cc421a8da3e94af3e31e6c77111fea0c76e40517348b0d8fd0f426
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

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a54b2e276662501dc9606ab28e4eb0bb9a2a419e5acc0d73402138911f0dc8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239156970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c11e61b4f99e9df57d4afcfd0fbf6a7687959b0143f0596a1ae29f095edef9d`
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
# Mon, 10 Nov 2025 20:10:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:10:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:10:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:10:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:10:33 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 10 Nov 2025 20:10:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 20:10:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:10:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:10:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 20:10:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32b34b6043df53356073fca74558aa4fb64fa2c3d92bc988ada13ba9600db416`  
		Last Modified: Mon, 10 Nov 2025 12:11:59 GMT  
		Size: 33.4 MB (33442309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e938140ec34eb319a6d20676b7a6e2f5d83fd145d7561a8dfd3c1aada2e67cae`  
		Last Modified: Mon, 10 Nov 2025 20:11:15 GMT  
		Size: 60.9 MB (60859335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458f584963d3e6c9c72a951017e5f3d071489e1ddc8d0ab9eedff42f76c43192`  
		Last Modified: Mon, 10 Nov 2025 23:14:39 GMT  
		Size: 144.9 MB (144852907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4867683b63be83d8c628c0c0406c48955dd2baabb811d5ec0b1bb5957789cd18`  
		Last Modified: Mon, 10 Nov 2025 20:11:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f86ede11ffdf851747fd312e3371f95197fa55f5d4122e778762727d08164`  
		Last Modified: Mon, 10 Nov 2025 20:11:09 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:43297337e6904bb9b9c1ccc060595897a5549457b37ad3099c4e764716e975a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5695882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f2b9e22917dcb29d6d98615ec9974ecb1025665450b17c2a8e9abea61a6595`

```dockerfile
```

-	Layers:
	-	`sha256:ec5f83a5ecb2ad6c2d9f9961df867980fb359b451e1d66154907366332055aca`  
		Last Modified: Mon, 10 Nov 2025 22:13:35 GMT  
		Size: 5.7 MB (5674542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb0622ec7e9301cabd6f58fade8651e1d28c1ba3535440e391cea8d5af691fc`  
		Last Modified: Mon, 10 Nov 2025 22:13:36 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2cbd057bdd95be4182a20c17c34f736cf58cb00c19c1c606a5b5e79207a2df90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235149289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4427ab61d8c2fc8175fa8cc0a21e9650ff4df5b4a3e6fafc74b5fe9ac05f5a`
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
# Mon, 10 Nov 2025 20:14:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:14:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:14:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:14:59 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 10 Nov 2025 20:15:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 20:15:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:15:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:15:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 20:15:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bcfce2f653765e7fbc0157676a8995e7c79e4d29c562744818763bd665844191`  
		Last Modified: Mon, 10 Nov 2025 12:11:55 GMT  
		Size: 31.6 MB (31555554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba68e38b628ced7f23a892e66f6c409bc4194d68eb342feec7cf35babe44ebe`  
		Last Modified: Mon, 10 Nov 2025 20:15:43 GMT  
		Size: 59.9 MB (59905919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dcbbf2ffb515aed448ee8610c3bec0f67efc3a5af738f1a6dd999c06afa38c`  
		Last Modified: Mon, 10 Nov 2025 23:14:22 GMT  
		Size: 143.7 MB (143685397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611183771ac572d38fa349fad0fc8842461763c4f36c11b7a4b9e94168d275d0`  
		Last Modified: Mon, 10 Nov 2025 20:15:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f733c84b076f068dbd2acee00c6445cda067ff3ce938345a297692e841a254`  
		Last Modified: Mon, 10 Nov 2025 20:15:35 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c9e5f6ebe7e26d97d7b5921029baae5eb880a643ea310ea0c19bb3aeb0480f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5695488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69ee4705ef928ba58e27d8c49097c7c3930b9398ada53c21cd33767ee053998`

```dockerfile
```

-	Layers:
	-	`sha256:91131e8dffd63257da53933001fda80e70c6522ba4147a2f6db24019839082e9`  
		Last Modified: Mon, 10 Nov 2025 22:13:41 GMT  
		Size: 5.7 MB (5674032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ad6566d4ec487faa6a164b2a42b6807073e8a621e7287ca95810282a072f2e`  
		Last Modified: Mon, 10 Nov 2025 22:13:42 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:16c08a5b5bda2d679a4b2e7f2f75ffa0cf4be0eb0424929a3ce9a5e333cb91dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245646170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da2954204e092218ac7d1c781783d7cc503ccf336cad7598a1602eda7eb02b5`
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
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 10 Nov 2025 22:24:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 22:24:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 22:24:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 22:24:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 22:24:03 GMT
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
	-	`sha256:34d4a3978004c899481865c404bd6f551fe978c88ec5051faef134232bfe1a81`  
		Last Modified: Mon, 10 Nov 2025 22:24:44 GMT  
		Size: 144.5 MB (144547822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e91f0818a356f701837ea6a8c0e8a69baac2adf676b8424d1d70caebe72215`  
		Last Modified: Mon, 10 Nov 2025 22:24:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e3d7c37e87c64c6c5a850174efeccbb082ccf494547d5dc181e07b5bada8b`  
		Last Modified: Mon, 10 Nov 2025 22:24:49 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:280c216306a26a4899e0f43fed1c500f637983e419c38fcc4fe8d5077cef1505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed51c079549f544345bbadceac66c8c3924be1397205705e423deb855ecf646`

```dockerfile
```

-	Layers:
	-	`sha256:6b2c481ec897b2cb0bce8987874f688980e6de41d1738a79822b3736729e838b`  
		Last Modified: Tue, 11 Nov 2025 01:13:25 GMT  
		Size: 5.7 MB (5661694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f5db45320ed1b639e7d3f969ae70f42c1c0d220846684ab576449da6146c045`  
		Last Modified: Tue, 11 Nov 2025 01:13:25 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:381546c6b1201aaf06bcf1dd915c52a0ff73fe0e0a08911191a9d55fcc98dbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229202929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2098f0209da8baab64a70c17d2366b6973463e2343d5650140dcf499596fee`
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
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 10 Nov 2025 21:53:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 21:53:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 21:53:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 21:53:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 21:53:29 GMT
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
	-	`sha256:0347b4ae32eb38cc5931c9599ad278746a10f46b2ad5a3586e1f9b0f0ccc2492`  
		Last Modified: Mon, 10 Nov 2025 21:53:59 GMT  
		Size: 134.9 MB (134862249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3073b04642cdd862d3b3a0884d30890603f8b12261cdd0bae559534e5584d8`  
		Last Modified: Mon, 10 Nov 2025 21:54:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1e3d85a4abb5a3d1c0c9eb1f76d7dd99494be6705d181d9d9c72dfe49dd421`  
		Last Modified: Mon, 10 Nov 2025 21:54:05 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f304c2dc01fe66842995b5cc69f8fdd497462fed0f27194a2de1e2dac0325ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5681408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1175701419caf9fab4cc4e506b43efd91a7a6437790e73db40e21892c462ff89`

```dockerfile
```

-	Layers:
	-	`sha256:b6042f309e26a9b5ed92c6f58620a9587f41ac03f8ef271337e059e2086b9c46`  
		Last Modified: Mon, 10 Nov 2025 22:13:53 GMT  
		Size: 5.7 MB (5660068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9db829dc01560d41ea242a4f04d52985b2b3edcb9a824c3b8ddf4b43c1ccf3`  
		Last Modified: Mon, 10 Nov 2025 22:13:54 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
