## `eclipse-temurin:17-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:888f16768fabf880f1a1317c6dccbbbe660706311bc47d6d092ec8c5ff6163a0
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
$ docker pull eclipse-temurin@sha256:285ec3398580de4b9cb7d57b684617a68a0c0356dfb800f387f23a8d560759b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236687915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2360cf886092ae2b485e753f39896872a639bdd371361605fc5bab49adb28008`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 17:11:09 GMT
ENV container oci
# Mon, 03 Nov 2025 17:11:10 GMT
COPY dir:b2070c3a584696dfa50295995b98f1ca6f69ef03e4ee4a779757baf0b56a1546 in /      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 17:11:10 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:11 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T17:10:18Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:38:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:38:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:38:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:38:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:38:29 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 12 Nov 2025 18:38:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 18:38:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 18:38:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 18:38:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 18:38:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2fb7c31c3da29493a9042fb2aac284034d054c3aa5fe92e1f234b9e077ede47`  
		Last Modified: Wed, 12 Nov 2025 00:12:41 GMT  
		Size: 34.2 MB (34167037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cc3ce36c7510a69dc987e7d0f1ee9c7b4c93994401d85bb4af03f8e05fbcda`  
		Last Modified: Wed, 12 Nov 2025 18:39:09 GMT  
		Size: 57.7 MB (57665587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23df4e197a0bc9e494620c640f7134e2c8860c92ef98ed1b6ff5257f28b2b2a5`  
		Last Modified: Wed, 12 Nov 2025 20:42:04 GMT  
		Size: 144.9 MB (144852873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0248b4fea83374378be20b25f66b364ab63ade4219295bbaacebf0e7fec887`  
		Last Modified: Wed, 12 Nov 2025 18:39:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec5459566de6c335c9ea04ab13d69b2b299e4ad047066b36ea924e1ef332aab`  
		Last Modified: Wed, 12 Nov 2025 18:39:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6e41c194ec52e8f145665efe58ec932a17e758c76704a65579063d3927de45ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ea26f186b42d03dddefb92d66a148d18f2e3472247ab376e945398579d5595`

```dockerfile
```

-	Layers:
	-	`sha256:76f7b61f0b1059d59f913ea24c630403433cae1dc7037778bd17c33e3bc2a963`  
		Last Modified: Wed, 12 Nov 2025 19:13:35 GMT  
		Size: 5.7 MB (5680904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b46cf6ba0c35f34c5c0797db5dc812b76198ea3ad46fcc980d5e910073e4f36b`  
		Last Modified: Wed, 12 Nov 2025 19:13:35 GMT  
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
$ docker pull eclipse-temurin@sha256:ae5c0fea8b00c8ece7d79d514bf586f958469af4cb861d149791813ed5ae82c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242464525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e14f004ac1fc02bec71a9c7f0d7129527f110009430be99998a7660081e398c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 18:21:17 GMT
ENV container oci
# Mon, 03 Nov 2025 18:21:19 GMT
COPY dir:bddbfbd27697aed0d6ba6e3639d53eb2bcbf54a469bc264141734564ee0873d3 in /      
# Mon, 03 Nov 2025 18:21:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 18:21:19 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 18:21:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 18:21:21 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 18:21:21 GMT
COPY file:db0b3bfc9b0c5f121f2453bb59e26e6e1b4ab566a800db9e34c541da8076e42d in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 18:21:22 GMT
COPY file:db0b3bfc9b0c5f121f2453bb59e26e6e1b4ab566a800db9e34c541da8076e42d in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 18:21:23 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T18:20:23Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:51:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:51:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:51:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:51:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:51:18 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 12 Nov 2025 18:56:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 18:56:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 18:56:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 18:56:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 18:56:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f0606a13920710459cad07c2d91ffb3bc0d8c2d18eb333131c2e90dc0ae025c2`  
		Last Modified: Wed, 12 Nov 2025 00:12:42 GMT  
		Size: 38.2 MB (38231260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c0fa2afff4fce2da3348f13f3ff118dfa655106daf72e83b8d728ab5a3304`  
		Last Modified: Wed, 12 Nov 2025 18:52:31 GMT  
		Size: 59.7 MB (59682969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c578596ed6d84ff1f878e53f00d5ca4946a131a5128bdc8e9607cce922a649e`  
		Last Modified: Wed, 12 Nov 2025 20:42:10 GMT  
		Size: 144.5 MB (144547877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3eb1da27513dea628d419b0da55a4737bba62d2dc71a57890ad2d5b52fa019`  
		Last Modified: Wed, 12 Nov 2025 18:57:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f4842b93820ade9751967dad041f024c66e20d0d4a907d9afa21c2b5ec33f`  
		Last Modified: Wed, 12 Nov 2025 18:57:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:edf0045dd3b9a580477b22fec48360a830861cf12958167dcb976e2f8c1d193b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5689432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b2a3dc6a4f3d88a63be5d07eeec95de669e4c1319881ccba29c7fd646283f1`

```dockerfile
```

-	Layers:
	-	`sha256:f5ddb501d8ba8741e1c378ed8c4006bd0ec4c33f33441a6538900dfbafe6d9a9`  
		Last Modified: Wed, 12 Nov 2025 19:13:45 GMT  
		Size: 5.7 MB (5668056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb6fc6edfc487a4d320d2ba3ef43ee8d4b4974ad58e0832924db2f50526def7`  
		Last Modified: Wed, 12 Nov 2025 19:13:46 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:a0785de94d0e3bdd26a82d866cb982eeac2696446fc0c2cdc7c605689d53f851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200317254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1485d1c8528b3052adb320a70ce625ff87d88ce7e763cdd6ab122651123b59`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 11 Nov 2025 09:53:26 GMT
ENV container oci
# Tue, 11 Nov 2025 09:53:26 GMT
COPY dir:9f1f5449cb9454b7c05550f990009868329830ff5f598e41882e09b2985f76ce in /      
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 11 Nov 2025 09:53:26 GMT
CMD ["/bin/bash"]
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 11 Nov 2025 09:53:27 GMT
COPY file:d3b5fde18206481b740a53df7391a42dcce042cfdd4edd5afeeb9637f6b9111a in /usr/share/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:53:27 GMT
COPY file:d3b5fde18206481b740a53df7391a42dcce042cfdd4edd5afeeb9637f6b9111a in /root/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:53:27 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "org.opencontainers.image.revision"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "build-date"="2025-11-11T09:51:11Z" "release"="1762851739"org.opencontainers.image.revision=0a583d401ee29f56bb3786d762c71b4349cd93d9
# Wed, 12 Nov 2025 00:25:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:25:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:25:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:25:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:25:26 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 12 Nov 2025 00:32:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 00:32:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:32:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:32:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 00:32:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1276be387a6a7c4ba51d350a6bfba6a1c72fe42d07414791e01dad4ca06bc732`  
		Last Modified: Tue, 11 Nov 2025 12:10:44 GMT  
		Size: 33.8 MB (33797474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94e9c54bbb60d78e3a1b2c270640fe5278b731547a8566cca26aacb7fbf74d5`  
		Last Modified: Wed, 12 Nov 2025 00:26:59 GMT  
		Size: 31.7 MB (31655122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce457af77e822ac03dd0de62c88167106f180815538a5f2b8a99b6a367f51489`  
		Last Modified: Wed, 12 Nov 2025 20:44:08 GMT  
		Size: 134.9 MB (134862237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f42f1aa61f6415b14aedbe83af628704f2f81307ce60abdf58d7e13841e487`  
		Last Modified: Wed, 12 Nov 2025 00:33:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d5a9a8bef4660454f70067d3a6e825c72c5648d2fc104e9053940168d183c6`  
		Last Modified: Wed, 12 Nov 2025 00:33:12 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3f8b7e20adc190a8409cd2b7914a704be7d032575f4bd7d32c3302e8d3d60b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3080362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636492c87dee1a88821a6f106fa6004dff93836680638a89e04aa2d411e5cc17`

```dockerfile
```

-	Layers:
	-	`sha256:e31280003c45d7d054d5b392a45dd9829ebf22723fa7d7856cb02e7b30328304`  
		Last Modified: Wed, 12 Nov 2025 01:15:05 GMT  
		Size: 3.1 MB (3059022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38d64cf3d6d927474c77d0e13a1690bc307fc11c33e13dad4a8b91c87978bf0e`  
		Last Modified: Wed, 12 Nov 2025 01:15:07 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
