## `eclipse-temurin:8-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:38e2cfe34b0003dfa64238baab581798e34f29d9d804cbe6da9373f5aab50c90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5d4e36d0e97caff94a789d855726755e0d26d20886c383fff0efeed8859a6279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127213233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63a7381d8e9cac52f0457d80ad28662d984f8db7adb0d9931879f2c4662a77d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 08:55:55 GMT
ENV container oci
# Mon, 02 Mar 2026 08:55:55 GMT
COPY dir:bc9a8a44e634605c4ff89328666c26f0c256afabea6c375c1017a88a80500ea2 in /      
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 08:55:55 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 08:55:56 GMT
COPY file:c0327936eac36593f0ab8d7da594e1a816cbe84da917c4d0a34bfcc7a914e024 in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:55:56 GMT
COPY file:c0327936eac36593f0ab8d7da594e1a816cbe84da917c4d0a34bfcc7a914e024 in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:55:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T08:55:38Z" "org.opencontainers.image.created"="2026-03-02T08:55:38Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T08:55:38Z
# Mon, 02 Mar 2026 22:05:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:05:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:05:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:05:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:05:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 02 Mar 2026 22:05:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 02 Mar 2026 22:05:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:05:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:05:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4377b1aab54b81e1e3b39331172fb1424f433cdfe28e8bf6f9cd313a971d0d61`  
		Last Modified: Mon, 02 Mar 2026 10:45:10 GMT  
		Size: 34.6 MB (34610905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f276e3eb8f3d45a8ee4d3cba66d483e300e92657d38599052823f1d516f222e4`  
		Last Modified: Mon, 02 Mar 2026 22:05:28 GMT  
		Size: 37.4 MB (37429238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fa804130ed113ad50a14e6cd025acf5e6649a6f6613c24dd07882fa739bc8e`  
		Last Modified: Mon, 02 Mar 2026 22:05:29 GMT  
		Size: 55.2 MB (55170647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad87534a5115b278e3f5be871dc859047f4e8af475fa96225db81fb58aaf265`  
		Last Modified: Mon, 02 Mar 2026 22:05:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b06b400e9aa4dbb2712425f9f184ab7a78312020bcc949d5172bc917d0f6b`  
		Last Modified: Mon, 02 Mar 2026 22:05:27 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b0d13795f8b7a4b1fc0c8d86c3576faa9f736495f15e937ae36dbc4782294197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6912d187c7373f6ee78dd0cebbd46350ed8c9217b29342ff6d69e8562248b94`

```dockerfile
```

-	Layers:
	-	`sha256:8a2a9183199d7bf9f59ceb6a056f253ff5c26352b3c474cb32bb08d16ea9fde5`  
		Last Modified: Mon, 02 Mar 2026 22:05:26 GMT  
		Size: 3.9 MB (3910756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb27d84c2b2e6c9ded3ef9727088c1dd99f0a4cfdf0b2e3df68890abfae815a9`  
		Last Modified: Mon, 02 Mar 2026 22:05:26 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:daf928ca4aa30f7819e32d08e7d4a15ca4d4b39caaa336909c10ffd96c03077c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124312055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6413fb5d16fe2dd80c2a4d895a5c289eed18b4c66c6f829dcbe61efb5575b3bd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 08:58:05 GMT
ENV container oci
# Mon, 02 Mar 2026 08:58:06 GMT
COPY dir:c8a0e6b85769dc5b1153f2d95c0dab0c21c76be6878d56a453a175f235aec4f0 in /      
# Mon, 02 Mar 2026 08:58:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 08:58:06 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:09f44631adf2e487fe312f2a1e81a1022d21dd1ab82974e6dcdb1c9761ad2ce6 in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:09f44631adf2e487fe312f2a1e81a1022d21dd1ab82974e6dcdb1c9761ad2ce6 in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:58:07 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T08:57:50Z" "org.opencontainers.image.created"="2026-03-02T08:57:50Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T08:57:50Z
# Mon, 02 Mar 2026 22:08:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:08:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:08:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:08:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:08:14 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 02 Mar 2026 22:08:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 02 Mar 2026 22:08:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:08:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:08:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ab71f30be3b758ee5a6fbf5d72df781f51e8cf5753ddf02671b2d7e13e4932fb`  
		Last Modified: Mon, 02 Mar 2026 11:28:23 GMT  
		Size: 32.7 MB (32683006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0a4bc094691173901df638d572125ecb683695471edf39a9b5416a19f8f4e3`  
		Last Modified: Mon, 02 Mar 2026 22:08:34 GMT  
		Size: 37.4 MB (37374516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6516c8949933997b17bd25101e6f8a114b92388392c92e2d7d400cf68739121`  
		Last Modified: Mon, 02 Mar 2026 22:08:34 GMT  
		Size: 54.3 MB (54252092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66010cd28322a986ed7f52b8272210f35919b887c53db1d970bdba87c33e2d4c`  
		Last Modified: Mon, 02 Mar 2026 22:08:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565081e6100b2a2375e8bc23752f6ea9de253ac2a441efc203c0051b0bd28a45`  
		Last Modified: Mon, 02 Mar 2026 22:08:32 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b13991a964faf876d6d72684bf02ea552986c4473c2a8d1bae237a82ddfa9f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e93740a280954b8d5de441d4ca97370a20cd0366fe23cb72a49987f3d6d1bd8`

```dockerfile
```

-	Layers:
	-	`sha256:83eed2372d9abd1d3190d90e815f61d388d672646cceae04e1cb2bb668606e2b`  
		Last Modified: Mon, 02 Mar 2026 22:08:32 GMT  
		Size: 3.9 MB (3910882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e629c2dab7eae01d8e7626c88c7ae5a6bc0ba33a8c07404491d1a1d539af422`  
		Last Modified: Mon, 02 Mar 2026 22:08:32 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:03262c7f16bfb951b62691c7998528bf68c1f1358cc011389066ee1e985dfdc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130567727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b3e28c01bdc364fc7a1f00a3a9a436008246e590eec62dffef0c179b10d4d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 09:04:59 GMT
ENV container oci
# Mon, 02 Mar 2026 09:05:00 GMT
COPY dir:e20d8c9b5112eae2ec3cf27567703617b532b3d50e37e22798356175a81af012 in /      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 09:05:00 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:f249adc52ffecf442b4262c353b6483cbd86a0119b4a0d56c2ae3482dda5e6dd in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:f249adc52ffecf442b4262c353b6483cbd86a0119b4a0d56c2ae3482dda5e6dd in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:05:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T09:04:48Z" "org.opencontainers.image.created"="2026-03-02T09:04:48Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T09:04:48Z
# Mon, 02 Mar 2026 22:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:11:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:11:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:11:17 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 02 Mar 2026 22:11:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 02 Mar 2026 22:11:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:11:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:11:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:52175d44fca07e14e1039fd9cb5b5c7a4f5a641951f3018cac642ab2b0d7aa2d`  
		Last Modified: Mon, 02 Mar 2026 12:12:22 GMT  
		Size: 38.7 MB (38730989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df108a302998b0b0c1beb639de829388ba26f170d0578e18c4fcfeb7e8204b`  
		Last Modified: Mon, 02 Mar 2026 22:11:53 GMT  
		Size: 39.2 MB (39183318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4677550d2e41116d94d59f88bb764520e569796c9449d0f7319973a3d605522`  
		Last Modified: Mon, 02 Mar 2026 22:12:01 GMT  
		Size: 52.7 MB (52650978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c19680a82545526994f61503b7bd77810e1f0f3a4ff29e55b4b010387a61874`  
		Last Modified: Mon, 02 Mar 2026 22:11:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4e4f8da4b123232a16e3fdda15505b261f793a2b073bb6a3edb5d603166531`  
		Last Modified: Mon, 02 Mar 2026 22:11:59 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:723b0080e69fab73538222f02f39274c8dd5d46633d9a4cf26834dd5acc1438a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3d1a9b89c9d0cffb98f9971855c48a9a7afccb357b1741de3962a6c22df7da`

```dockerfile
```

-	Layers:
	-	`sha256:9d75c6c1cb25c137fd10959caed918fe0f125f6333d1dfca0f5c59755acf73f3`  
		Last Modified: Mon, 02 Mar 2026 22:11:59 GMT  
		Size: 3.9 MB (3898183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e48b9f82f1db6a4f0b3b01885e97e110788146d63229455cdacbeb2cf2fa6c3`  
		Last Modified: Mon, 02 Mar 2026 22:11:59 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
