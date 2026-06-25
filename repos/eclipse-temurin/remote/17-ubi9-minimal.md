## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:d19e9b5046cc66e394bb1a47770912cb96ba0a9b9c068c66869f1f77918012a0
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
$ docker pull eclipse-temurin@sha256:200e97349c21f5708354906496a20c2efc8bb8cf274560c5b767f98fdb6c1183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.2 MB (214249365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7aeea30f8bb3018afc2bdcf3221540fcf62b7282fe0b4d7c74f76b548419bd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:04:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:04:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:04:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:11 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 24 Jun 2026 23:04:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:04:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:04:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:04:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:04:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24c036af34f598a58e314ee2d700bce8c8f29eb9ba1eb87d20ef7c72cc6d481`  
		Last Modified: Wed, 24 Jun 2026 23:04:36 GMT  
		Size: 27.7 MB (27660377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd763b861de03232f27061726ca7f5b8519580a22e7431c9a608cb17faa1a4`  
		Last Modified: Wed, 24 Jun 2026 23:04:39 GMT  
		Size: 145.9 MB (145915434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9757bb4371d01306c075a0704daece7f7e6b190f0d874fdc3860f3325f28d90`  
		Last Modified: Wed, 24 Jun 2026 23:04:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65468532f006fc3f40af7e8f4618e0b8860ea0152aa9434634e945d6fcdc6b0`  
		Last Modified: Wed, 24 Jun 2026 23:04:35 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9ae73be44b11271284fd3fd07c885d2771c41f6d8fac2626cbcfdc29e6f4e65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c4c8f3760066a315e80466cd0e21a83860f95f01044cfa970f14a277bd1846`

```dockerfile
```

-	Layers:
	-	`sha256:7b429c34fb544189700331dd9b119b6166dd26353e0ece02eb15aa585fdd1fc6`  
		Last Modified: Wed, 24 Jun 2026 23:04:35 GMT  
		Size: 2.5 MB (2495118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec05e0ffeb3f4b76608307c0fb0ad23fbe8e7669b899621f4ed309faa2729f33`  
		Last Modified: Wed, 24 Jun 2026 23:04:34 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6fbd0cd5727012fe8a4a41615e4f0d7d0326f7985b209d334db5bf6ffb572bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 MB (197602538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165a142b9af691999c77ffeb11aa422226b25df266aae612eb8cca3321169735`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:03:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:03:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:03:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:03:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:03:28 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 24 Jun 2026 23:03:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:03:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:03:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:03:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:03:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f865cd6d1ffb45d45ffc07c7c7475127decf80db90d306d391f28554b99278e`  
		Last Modified: Wed, 24 Jun 2026 23:03:53 GMT  
		Size: 14.1 MB (14059478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7771615684576a5f5986d7ded414c3a765544d17c15ca98b8d9833adbd59eff6`  
		Last Modified: Wed, 24 Jun 2026 23:03:56 GMT  
		Size: 144.7 MB (144734818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10162f71f28a44e9352d35403f77546b610484e6c5c7f32ba898974148724d4`  
		Last Modified: Wed, 24 Jun 2026 23:03:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc45e288ae846bbf7915c33a0a9eb3068f5b4c9ce81b8b5344c334edc1614e5`  
		Last Modified: Wed, 24 Jun 2026 23:03:52 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f320a7b574fa37c05c9a88a50b49eafbfb1ad9768abaa51f326c20966b2def81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1777606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd514733d86359a972d60eb16072aa0b9b3a97f31054e99479e65646ff2cad`

```dockerfile
```

-	Layers:
	-	`sha256:ba432e29e1112e5746b4ea5c70f24b2aa3320d9aa8861e81abdf356c19ff244a`  
		Last Modified: Wed, 24 Jun 2026 23:03:52 GMT  
		Size: 1.8 MB (1756322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4172d71f48fbb48039f3a700effa1f1289b69a63e51e1fa8ce6d9da1b06b5fd8`  
		Last Modified: Wed, 24 Jun 2026 23:03:52 GMT  
		Size: 21.3 KB (21284 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:880a2c7e4b9fc7a3c3062ade94c0ef84cd4124dc8fe9f19caa6451e9824f064a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206093703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ad562f99c0d4dad59f43236cb2c2f4ec4ba50ad3830e5c6e7661c98e141137`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:13:01 GMT
ENV container oci
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:4d2a3ebfba3e6886b6504d8dd92beaac194e548e40aa4bca182adbaa9be02afc in /      
# Tue, 23 Jun 2026 05:13:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:02 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:b7827d131ad066b0f131c7ebfb16ff261b70c3cbb8cf357ab0913f8aa1eef055 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:b7827d131ad066b0f131c7ebfb16ff261b70c3cbb8cf357ab0913f8aa1eef055 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:02 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:46Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:46Z" "architecture"="ppc64le" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:46Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:01:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:50 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 24 Jun 2026 23:05:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:05:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:05:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:05:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:05:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4bac72a9a1f43367def803d06c2dab63b4bb0e322cb08ee3db80259d84e62045`  
		Last Modified: Tue, 23 Jun 2026 06:12:06 GMT  
		Size: 45.1 MB (45144751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f99e1bd1d0e0245b9ff9de06dc4f155f0170e63761b11e9c13863eabbea391`  
		Last Modified: Wed, 24 Jun 2026 23:02:32 GMT  
		Size: 15.2 MB (15157790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ab39c20473d0b082642d3a1836179b006ce6ab514422785a61b787c20a7fda`  
		Last Modified: Wed, 24 Jun 2026 23:06:36 GMT  
		Size: 145.8 MB (145788742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb84942fb410750eed5a63348a98ef297c21d806976dbf7cd3f724bbee28e49`  
		Last Modified: Wed, 24 Jun 2026 23:06:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb13ce8a4cd9e21563ec16f9ffc1f1da7672fd6440aad033f492e6a164093e3d`  
		Last Modified: Wed, 24 Jun 2026 23:06:32 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3fc3a3bf7e95ed4b9f6e4b05c9818b57f98cf00cb1d9458bcddbec7fe7212294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1777430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188c13b05597e3770aff1e8fa63557dffc08e9a070f95e6203c7c988d434ee24`

```dockerfile
```

-	Layers:
	-	`sha256:52916b29288e53192be6b208a19aabf4a6479232ffed25bfbc369fefca4d75dc`  
		Last Modified: Wed, 24 Jun 2026 23:06:32 GMT  
		Size: 1.8 MB (1756226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f96bda0af84da8b8b1dc2f605eafa173c93593d90b7559b73c2dd4907bf928`  
		Last Modified: Wed, 24 Jun 2026 23:06:32 GMT  
		Size: 21.2 KB (21204 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b70a9d4e926d8490ed2d06f7d4a82d35dad998bfae5cad165272bbb0e99447a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188561069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2060e54758e258d16e1d3ea5aeb17aee9795f12d3da97eb651816fba14f8cc55`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:18:00 GMT
ENV container oci
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:27877c357368aea512a88a6f3ff986d2f2cae38facf5c958fc65210886393092 in /      
# Tue, 23 Jun 2026 05:18:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:18:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:93599b4d15b0e179c067caa1878c815ffdcb1bde2382dffed0b86ba833b3047a in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:93599b4d15b0e179c067caa1878c815ffdcb1bde2382dffed0b86ba833b3047a in /root/buildinfo/      
# Tue, 23 Jun 2026 05:18:01 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:17:03Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:17:03Z" "architecture"="s390x" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:17:03Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:01:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:53 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 24 Jun 2026 23:02:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:02:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:02:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:02:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:02:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:027b6558e15fa03e681ac683754dd2058185e2be499788f5e5a422bfa61b34db`  
		Last Modified: Tue, 23 Jun 2026 06:11:50 GMT  
		Size: 38.8 MB (38754261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ba193d3988998f0967fb407a4f53a44e2a2ac7df01730ea0a45fcebd52490`  
		Last Modified: Wed, 24 Jun 2026 23:02:22 GMT  
		Size: 13.9 MB (13892087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6d53f0675ed082600f6a655cdc066e791ba576ed23717c8b2d29b87c6c3fa0`  
		Last Modified: Wed, 24 Jun 2026 23:03:08 GMT  
		Size: 135.9 MB (135912303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e3f291d41684b361c01f8e1f348646eb0393252d7630d276ab1f0415d886f6`  
		Last Modified: Wed, 24 Jun 2026 23:03:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a9e0c4aea37254678d7114c9e20d482a31868bfb26391ec55f5cf72cc809d3`  
		Last Modified: Wed, 24 Jun 2026 23:03:05 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cc11a82f503c7b3333656e0b1e76f47e64260c013b4ec0940c3231c22261ee17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14a9287a293dcd4dfa3425776a4d6d7a383942c553f7f2995f0e57fcc088bca`

```dockerfile
```

-	Layers:
	-	`sha256:228aff296a2fc67cf90268c1f5e671aaa7767c90067bed81452dff2dd9c889be`  
		Last Modified: Wed, 24 Jun 2026 23:03:05 GMT  
		Size: 1.8 MB (1754984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a340a7b089801dee7c4c29ea81bb78247251e007e50043cffbc124afeefdd53`  
		Last Modified: Wed, 24 Jun 2026 23:03:05 GMT  
		Size: 21.2 KB (21165 bytes)  
		MIME: application/vnd.in-toto+json
