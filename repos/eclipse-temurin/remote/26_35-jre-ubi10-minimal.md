## `eclipse-temurin:26_35-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:5658b95d753323f9107d16f584f8645b13b1ea93e9c1db006b99232875cdaea5
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

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2f0d11027bd806b3c59dbd094bf0bead0d8c0432928482a5839252bde0b833a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136426139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cf74ef8595217b12017d308a9680a87fb3ed8d595949ff52433ae75d32ee0d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:14:03 GMT
ENV container oci
# Mon, 13 Apr 2026 09:14:04 GMT
COPY dir:76b09a495622d7b6331e3b1ce0727af742be820fe3eaf865e896be5c160bcdbe in /      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:14:04 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:95047be8e40b1e3c668ac62dda8bcb33d863723da6a80c1b3ce4f34f04292a93 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:95047be8e40b1e3c668ac62dda8bcb33d863723da6a80c1b3ce4f34f04292a93 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:14:05 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:13:50Z" "org.opencontainers.image.created"="2026-04-13T09:13:50Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:13:50Z
# Mon, 13 Apr 2026 23:59:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Apr 2026 23:59:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Apr 2026 23:59:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Apr 2026 23:59:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 13 Apr 2026 23:59:48 GMT
ENV JAVA_VERSION=jdk-26+35
# Mon, 13 Apr 2026 23:59:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 13 Apr 2026 23:59:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Apr 2026 23:59:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:59:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f0c6a9d8564d2a3d188b4b49db41fad56fb7e4756edf376c0ff881d93ab0da5e`  
		Last Modified: Mon, 13 Apr 2026 10:09:42 GMT  
		Size: 34.6 MB (34605867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b6861fdd7946506cc94e08e3679108e5428d27115af7376fbe39e7aecfec14`  
		Last Modified: Tue, 14 Apr 2026 00:00:13 GMT  
		Size: 37.5 MB (37460448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1596c497be6630eca2433878759e7a2016ba583c429ab39ea8a1a2f057e29b39`  
		Last Modified: Tue, 14 Apr 2026 00:00:13 GMT  
		Size: 64.4 MB (64357407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891243b22e7bcb54ee4bf9cd1fa72e499192e96a69ef82ee8dbc23e59004bba0`  
		Last Modified: Tue, 14 Apr 2026 00:00:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8f29900b946e3f0672984c48960661311117dcc75faf1a15a96bba369685cf`  
		Last Modified: Tue, 14 Apr 2026 00:00:13 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:311164d7442109e05d0c7389f602019e9254dbdd1e6e10cbc5c5398a4fe01e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c9e9aee0c0af126f315a6fb4a07ab2dd57c0338fce415f385881126121106d`

```dockerfile
```

-	Layers:
	-	`sha256:60a492a229e9e8ba2f4e4df8739e5cbf0c9d15a8ca8332f62f66d762082e61b4`  
		Last Modified: Tue, 14 Apr 2026 00:00:13 GMT  
		Size: 3.7 MB (3711614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d544ac78f8992ec19a0435e4eba1ff71df8a398f1557317bbe26bb3dd2e11d68`  
		Last Modified: Tue, 14 Apr 2026 00:00:10 GMT  
		Size: 20.3 KB (20258 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3183b8ee8b3a0f58484d7eaf5125ad2e9d807fffe4b72a9c555da5699a7b1253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133329456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c95089e5fac86957145c3586ca18fd0088e278d7cbbca736fc9cbfb075d0428`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:04:43 GMT
ENV container oci
# Mon, 20 Apr 2026 01:04:43 GMT
COPY dir:3dce53cd7f9d7326227f9f135d7cd4905e49967e75fffdb7305248967fd08ecb in /      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:04:44 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:47b968046aebceb7e689b8f162b1d58465b394d88fb7d588f40ffa5eb8594d57 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:47b968046aebceb7e689b8f162b1d58465b394d88fb7d588f40ffa5eb8594d57 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:04:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:04:27Z" "org.opencontainers.image.created"="2026-04-20T01:04:27Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:04:27Z
# Mon, 20 Apr 2026 23:04:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:04:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:04:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:32 GMT
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:04:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8aaf81d11ba9b2394d31694793b5dabaf4eed2f5a356c7de160384c76fcf3161`  
		Last Modified: Mon, 20 Apr 2026 12:17:52 GMT  
		Size: 32.7 MB (32690247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3d536a921f9a95e68bbfecbeaed496bd3d42de4eb02a54248ea19d276ccab1`  
		Last Modified: Mon, 20 Apr 2026 23:04:55 GMT  
		Size: 37.4 MB (37401972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb7de5a025715d08ba8abc56ae9df5b758d085d81b21bb5ac2198498198cfb7`  
		Last Modified: Mon, 20 Apr 2026 23:04:56 GMT  
		Size: 63.2 MB (63234820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e77b9a7a71a5151806336bda824106958f014ced73c7b2eb5ecc3c19771e64b`  
		Last Modified: Mon, 20 Apr 2026 23:04:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b06276767ff582a43fdd07e18b8ed9197793c8400e2401e7c3f321cadd131b`  
		Last Modified: Mon, 20 Apr 2026 23:04:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3b43eb1f885f9791e05418461638c87935e53f7f212f96021e062499c6cef4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94885f000c06e49db3e818de8987467d30e1f7e375207ab8943d5d0f412d0b77`

```dockerfile
```

-	Layers:
	-	`sha256:7707084cb82ebe8fc8b897b3078bcc8ea6767bd2e895d28ef37e96b99c37bfc6`  
		Last Modified: Mon, 20 Apr 2026 23:04:53 GMT  
		Size: 3.7 MB (3711025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625e071435fa234f712a32deda048530b12c18564b1bc15363e5ca0be60c751b`  
		Last Modified: Mon, 20 Apr 2026 23:04:53 GMT  
		Size: 20.4 KB (20362 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:49e74ccd7d06c3289e4df7189a8e2ed724cdc05a38ecdc101482fcf89df7dbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141642220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6116d4be8522f739fba0245097c23b6ec9b6cc1a1023aa93e06d30b51b8e19`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:15:35 GMT
ENV container oci
# Mon, 13 Apr 2026 09:15:36 GMT
COPY dir:d5bea9ef78808f560c142c54c074655a9c233520184b1046a8e6bef1925013a7 in /      
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:15:36 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:ef9ee329c018a2f17a5a5c4723c1803a667108705d8c3d16152fdcce104fca5d in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:ef9ee329c018a2f17a5a5c4723c1803a667108705d8c3d16152fdcce104fca5d in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:15:37 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:15:24Z" "org.opencontainers.image.created"="2026-04-13T09:15:24Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:15:24Z
# Mon, 13 Apr 2026 23:56:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Apr 2026 23:56:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Apr 2026 23:56:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Apr 2026 23:56:07 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 13 Apr 2026 23:56:07 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 00:01:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 14 Apr 2026 00:01:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 00:01:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 00:01:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6ab9c9492755280705c94f3f242c73ae33058d432445b818684063f12da4648d`  
		Last Modified: Mon, 13 Apr 2026 12:12:34 GMT  
		Size: 38.7 MB (38703789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635d84f1d74aebc8b054009ce82709f7f82d78dc2ec7a147aca9cfbbd6cd6ba`  
		Last Modified: Mon, 13 Apr 2026 23:56:49 GMT  
		Size: 39.2 MB (39213284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4ae2a4097355f33684d4a3adcbf4f577424903c5ca70f2f85edaf86c18e66c`  
		Last Modified: Tue, 14 Apr 2026 00:01:53 GMT  
		Size: 63.7 MB (63722728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6479263edde4fe489e2c39c83573353e1c29ceeee36d4f5ca7878ee72b8b76`  
		Last Modified: Tue, 14 Apr 2026 00:01:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12983c3fc67835f19cc0cd007c842b581b24f6ee3361425244b689b6605a2c25`  
		Last Modified: Tue, 14 Apr 2026 00:01:51 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:27c18ab8186f4d9f81baf6002dc36228844fd9ba57b7d22f4cfd723c37de3476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a283a83154292fe83bd08f18a3c18bd71a81c320d82607a86839a2b170a215`

```dockerfile
```

-	Layers:
	-	`sha256:5c5bc07e0940aca89c3b725da255cd879c699810b9e1ddaab843cb7d4429d010`  
		Last Modified: Tue, 14 Apr 2026 00:01:52 GMT  
		Size: 3.7 MB (3699738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ef8d69cf29fee4bce80d6d33a1c1ba399c72ee6f591c88d899b20749395337`  
		Last Modified: Tue, 14 Apr 2026 00:01:51 GMT  
		Size: 20.3 KB (20288 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:46b4409c0203edb11e68aa8d61ee31050784c4c9f6c79bd76d7d7c308b0b2d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134344695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101524552b411a218dd950836e3be80a690e193a9c8db84d5e5bec259141d6f5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:25:38 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:25:38 GMT
ENV container oci
# Mon, 13 Apr 2026 09:25:38 GMT
COPY dir:ad109b9d5b6b27b6a32c6164256d49555b57cad980ed41bb7919f46c193548d7 in /      
# Mon, 13 Apr 2026 09:25:39 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:25:39 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:25:39 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:25:39 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:25:39 GMT
COPY file:96d9bfab384c8f83c1e861826c245cfcf0f99bdc60feb690e105ae848d35845f in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:25:39 GMT
COPY file:96d9bfab384c8f83c1e861826c245cfcf0f99bdc60feb690e105ae848d35845f in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:25:39 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:25:24Z" "org.opencontainers.image.created"="2026-04-13T09:25:24Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:25:24Z
# Tue, 14 Apr 2026 00:19:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 00:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:19:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 00:19:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:19:58 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 00:21:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 14 Apr 2026 00:21:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 00:21:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 00:21:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8f5978fd2681e854c13e31fbe180a315ce298fbb55b1eeaa5273a755fa9be12e`  
		Last Modified: Mon, 13 Apr 2026 12:12:27 GMT  
		Size: 34.4 MB (34428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcd429d51dc25a5fbc74461478fcf357bd2876473eb7e65bcbc968b761e6886`  
		Last Modified: Tue, 14 Apr 2026 00:20:25 GMT  
		Size: 37.8 MB (37842843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292bc49382329854d543616217f7458644ea3aa6c67df2d2d639b3a6b69b7926`  
		Last Modified: Tue, 14 Apr 2026 00:22:12 GMT  
		Size: 62.1 MB (62070634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5f473dc71b5c181fbd25b0519913065b38b6fe57f89f5ae2035a673a22cfb8`  
		Last Modified: Tue, 14 Apr 2026 00:22:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0192efa41d9f91e2bec22d5e5513387aa5b2263878fd3c68c1ef97a5dff1a`  
		Last Modified: Tue, 14 Apr 2026 00:22:10 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dc9316347fe5f164c67fee1394dc4428a2089cd1bc15cab6174d089e9e899b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d18554eeb7a753981be37b174a868afb50aaa41aca87894ccd7b177daaea9d2`

```dockerfile
```

-	Layers:
	-	`sha256:1277c4e367b58d54689963a90a883f9601178a5982aaa6e298a0f7407c748dfd`  
		Last Modified: Tue, 14 Apr 2026 00:22:10 GMT  
		Size: 3.7 MB (3700983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f9016ef4cd592cff7d3d4604b5414770b0c8ae8eeaaabf5049e48b89facde7e`  
		Last Modified: Tue, 14 Apr 2026 00:22:10 GMT  
		Size: 20.3 KB (20258 bytes)  
		MIME: application/vnd.in-toto+json
