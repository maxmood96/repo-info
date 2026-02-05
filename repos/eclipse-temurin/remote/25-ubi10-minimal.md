## `eclipse-temurin:25-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:0922de8b12139cdd76383eb576dcedc965f2ae5a74c07a291ecebf9a9da016fe
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

### `eclipse-temurin:25-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7765b8e5a82092813de8c9c3f8b27d1e309ac58b2ef2483ecb1963763a3b4e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164028157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baf18050a6290699cbfa1909cede04201ed6bb1f69a333cb953f1f3a9096c04`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:55:06 GMT
ENV container oci
# Wed, 04 Feb 2026 04:55:06 GMT
COPY dir:ab88dbc5c421721056a4539f41aea4ce909f7032f536329269fb1718e0c3e67d in /      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:55:07 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:6cb7b50636b55f291cf75a2750279d2c83bd2761ac9a492a49d90a49cb72e8ac in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:6cb7b50636b55f291cf75a2750279d2c83bd2761ac9a492a49d90a49cb72e8ac in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:55:08 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:54:43Z" "org.opencontainers.image.created"="2026-02-04T04:54:43Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:54:43Z
# Thu, 05 Feb 2026 00:07:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:45 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 05 Feb 2026 00:08:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:08:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:08:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:08:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:08:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:819501e18c85a616b033a682e2078167e38cd15970dd3534932af6715532259f`  
		Last Modified: Wed, 04 Feb 2026 05:56:28 GMT  
		Size: 34.6 MB (34565108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec578a5b872ff3963269dc8b3c9c42e6a07d9d14435675e21d6db4154387d9c`  
		Last Modified: Thu, 05 Feb 2026 00:08:03 GMT  
		Size: 37.4 MB (37413931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046a727efbe9a88a8dd2a8aad47dade9d33639d982f08b524f37658e22631385`  
		Last Modified: Thu, 05 Feb 2026 00:08:57 GMT  
		Size: 92.0 MB (92046700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866a48df224589b94ca0de88236334226057935d5a7a0f03c4d02b1391924bc9`  
		Last Modified: Thu, 05 Feb 2026 00:08:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e689e6bcef162fc1cff06345d321b81c37dfd98713dcb9af349016799b94313`  
		Last Modified: Thu, 05 Feb 2026 00:08:55 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0decf8b39203f58f1622bd6bf544144568ab0de12c88fc5ecfe1e16cb85d29d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ecc29a0cff6cc0744cf93fc38bcee507d8938aa91d7701cdda5b7757d483b9`

```dockerfile
```

-	Layers:
	-	`sha256:4a3e5086a5445295adfb4f0b2394bd785653c5ad8d3855344c9c69d0d458470e`  
		Last Modified: Thu, 05 Feb 2026 00:08:55 GMT  
		Size: 3.7 MB (3739171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1aeda2cf0366ea81c94d8b270810723749a8568f08f76dd568a8af5fde1d268`  
		Last Modified: Thu, 05 Feb 2026 00:08:55 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e06ef1209b65716ce22646c5c43349907e8ab24b874510899f532e9bb0091072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161081509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d693c83e45685febfb72c2fb76474f63ec87c7de898dadcebd4e210a00504caf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:56:41 GMT
ENV container oci
# Wed, 04 Feb 2026 04:56:42 GMT
COPY dir:67028d43c1066b84b1209232f64f1a4cc4b9dbbfba57178bd9cbb9c32d30e9e7 in /      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:56:42 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:6daaa71ff7be172f731620b1d0190bb9c2177930f1dd64e2221f2ce09f100fc6 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:6daaa71ff7be172f731620b1d0190bb9c2177930f1dd64e2221f2ce09f100fc6 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:56:43 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:56:21Z" "org.opencontainers.image.created"="2026-02-04T04:56:21Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:56:21Z
# Thu, 05 Feb 2026 00:07:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:34 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 05 Feb 2026 00:08:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:08:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:08:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:08:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:08:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e7aaef72f9aac8066ddd0c18bcd7c76fcc63212a965d38f195e0959c666aa7ce`  
		Last Modified: Wed, 04 Feb 2026 06:11:32 GMT  
		Size: 32.7 MB (32661097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8ce8973f77525b79ed12550746b2d685f318d171203862037d5f55886153a7`  
		Last Modified: Thu, 05 Feb 2026 00:07:52 GMT  
		Size: 37.4 MB (37361697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0e3222de8476ba8d8be571a69387b6b7d36660a38893ba441ccfb44d130a85`  
		Last Modified: Thu, 05 Feb 2026 00:08:25 GMT  
		Size: 91.1 MB (91056296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f6cd2145875be92660182e88aae5f56cfdcad2ee04e72e32e943d02e2b319d`  
		Last Modified: Thu, 05 Feb 2026 00:08:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4e8e6f8364939b0ef795d340e862b76e81fd5be42e71eb8f5c6e92bb3ddac4`  
		Last Modified: Thu, 05 Feb 2026 00:08:18 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ca71d447643d2b4a784b88c52770d737d11220803d34c043c20930a8591a23ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3744d3be219926e22cffe4b8a46d6b51b70c59fafd2279ac70a1aaf1ca7a9f42`

```dockerfile
```

-	Layers:
	-	`sha256:c4a4a84c7e43ce1d4120082c2a4b1e28bdab77ab2afc1ad243272658fb75a5d4`  
		Last Modified: Thu, 05 Feb 2026 00:08:23 GMT  
		Size: 3.7 MB (3738594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de0bb278e51f4786dc6d7e2fa4410fcb0035b416329362cd14771a385734900`  
		Last Modified: Thu, 05 Feb 2026 00:08:23 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:43d8314f45bca17b3f78674376e36edf24013c78a17f0b45fb7d9643f0517f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169477090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec528e7e28f616f7f1582bbfd6ec342a4c39461afcf9c46d8902a5bd10212da`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:58:36 GMT
ENV container oci
# Wed, 04 Feb 2026 04:58:37 GMT
COPY dir:09fdad4b579363b2c8418a42c62ea4dc38d67115c8d53cd4a2ec14253ecaf9ad in /      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:58:37 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:0c67174697cfbd406f6852cad47660b65db0ae88b3ec344fd5c165877edf759b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:0c67174697cfbd406f6852cad47660b65db0ae88b3ec344fd5c165877edf759b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:58:38 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:58:25Z" "org.opencontainers.image.created"="2026-02-04T04:58:25Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:58:25Z
# Thu, 05 Feb 2026 01:21:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 01:21:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 01:21:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 01:21:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 01:21:18 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 05 Feb 2026 01:50:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 01:50:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 01:50:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 01:50:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 01:50:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1cff691ae927c200ee804ea0243a79390de10e4d7f5f6687bde708134b9917c4`  
		Last Modified: Wed, 04 Feb 2026 06:11:59 GMT  
		Size: 38.7 MB (38689551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a9332059e30e789362eb783b19695b44bab5a28726fe9fd59ec73d342defd`  
		Last Modified: Thu, 05 Feb 2026 01:22:04 GMT  
		Size: 39.2 MB (39172221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5059341d80e55d902cd3ede4e927cea2f97f35af7df1188514babfb4bf35c4`  
		Last Modified: Thu, 05 Feb 2026 01:50:56 GMT  
		Size: 91.6 MB (91612900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a782c2cefa7ca0b0673986fd5e1c9a6ebe49f3eaeea96c60d375d80535f87b`  
		Last Modified: Thu, 05 Feb 2026 01:50:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45f3624971eafe35eb630abc0570f54c2f4609550d9d7a03f8da04330632430`  
		Last Modified: Thu, 05 Feb 2026 01:50:54 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ab661c1609993278024f0dbdefaf0e3ee2cb7f08d85de18279fad22dc1099c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb031a7ad31862bda5e263378150ef464fa0dd6d3b4d47338249bb00f7dfbf4c`

```dockerfile
```

-	Layers:
	-	`sha256:32551c247b986a48a44e66dc703143aa0046820957ca3f0ab082c8474e4aab20`  
		Last Modified: Thu, 05 Feb 2026 01:50:54 GMT  
		Size: 3.7 MB (3727301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea66b721028e93ffe199822d27c8ccad5acebf8406ce5ec24ecf0ddb60ee2426`  
		Last Modified: Thu, 05 Feb 2026 01:50:54 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:2d0f3e0df8b15e6d5843810b7c91f6c30689714bc51a745f28f96d52ab71f2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160408227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965a2fd0e0325ecfe0e7e5ea7f7c4a2be07a360c5eb1c2ea15eab6830f24bada`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 05:11:29 GMT
ENV container oci
# Wed, 04 Feb 2026 05:11:30 GMT
COPY dir:9d4ac575a92f53870377be4b68b1588c9bc427ee283102569774f3d9158a16f9 in /      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 05:11:30 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:bd2f18d5b9d97db31e1a3f98a0670c0f15ee13ca2c036700589166ed0ad3221a in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:bd2f18d5b9d97db31e1a3f98a0670c0f15ee13ca2c036700589166ed0ad3221a in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 05:11:30 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T05:09:09Z" "org.opencontainers.image.created"="2026-02-04T05:09:09Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T05:09:09Z
# Thu, 05 Feb 2026 00:07:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:02 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 05 Feb 2026 00:10:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:10:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:10:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:10:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:10:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c5e6ba1d838b1d4e103e0457068eaff01f71c8436e4442eaa2f5c701ccbe1c6`  
		Last Modified: Wed, 04 Feb 2026 06:11:43 GMT  
		Size: 34.4 MB (34399700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19d1328bf4040759158c3f4a9ecc47912b1ffb1b173eb92519cea4b9d9c9de`  
		Last Modified: Thu, 05 Feb 2026 00:07:35 GMT  
		Size: 37.8 MB (37794412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34a834de18bf02232512c5494adb2222bd56898f4d565389d84046adc1a9ee2`  
		Last Modified: Thu, 05 Feb 2026 00:11:13 GMT  
		Size: 88.2 MB (88211700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f747fe0e3208d0e332c5d0e4a9b50d0ccf77593ec9d65b0ee743d0ed274108`  
		Last Modified: Thu, 05 Feb 2026 00:11:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e2c945bfecc2c2a97713fc0fc24f5ff45dad3649495b5c50a1b54da59f39f`  
		Last Modified: Thu, 05 Feb 2026 00:11:08 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d55bcdf567399b8896b4fa9e6aca7244c9f1518a28e2a000c418db74073d97b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8890ab7ae045fea75c17b0cf539655c014b5125c6c2bdd82a979a501e8a9d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a5d920e2136a39fc2e06b29e69343509918b95e49b68ef67796bdb69001d32f0`  
		Last Modified: Thu, 05 Feb 2026 00:11:09 GMT  
		Size: 3.7 MB (3727309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636e9c31f87c1e4e60b2898cfb5b618b9b359df17b7f2541e5a03e65aec2614e`  
		Last Modified: Thu, 05 Feb 2026 00:11:08 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json
