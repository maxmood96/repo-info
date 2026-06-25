## `eclipse-temurin:17-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:c3fddf9d704a6fc1f04bb6e660b7facaeeb64d456a6e2a49e0e223f4c7a376f6
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
$ docker pull eclipse-temurin@sha256:1e43ab18685d6ec199430c9a15fd3cf77f0d88b32d5df6f19e902d5074c47332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218560241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb471393c50ba916c6bccff927781954b6649179685fe49515176ba0318769e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:40:14 GMT
ENV container oci
# Wed, 24 Jun 2026 06:40:14 GMT
COPY dir:92709e786f8e662d73459e8ec6b629a535dce92ae9fcad21b6d7b00ac6803604 in /      
# Wed, 24 Jun 2026 06:40:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:40:14 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:40:14 GMT
COPY dir:e8e2b7cb869a17d32d7452a63fca2737847da7b62b5d0406fabbac5267964ccc in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:40:15 GMT
COPY dir:e8e2b7cb869a17d32d7452a63fca2737847da7b62b5d0406fabbac5267964ccc in /root/buildinfo/      
# Wed, 24 Jun 2026 06:40:15 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:39:51Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:39:51Z" "architecture"="x86_64" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:39:51Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:04:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:04:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:04:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:04:10 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:10 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 24 Jun 2026 23:04:16 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:04:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:04:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:04:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:04:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d16bd660d5aff2d8cb434aefeedc41e2a96fcbfce0e10b612181d05ae773b985`  
		Last Modified: Wed, 24 Jun 2026 09:11:20 GMT  
		Size: 34.9 MB (34866797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff0e28da6546f731fad83fec8cc93f8359452a9f724c32b111319f4eba4eff3`  
		Last Modified: Wed, 24 Jun 2026 23:04:36 GMT  
		Size: 37.8 MB (37775596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a459ee556fccc5903d143709aaa9b07f72fedfcb0c2bef70e6da88944a66fb08`  
		Last Modified: Wed, 24 Jun 2026 23:04:39 GMT  
		Size: 145.9 MB (145915428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f28467bd8927346c1b03252a50f3b8c6bac94a32991df30cbfa09c83004156c`  
		Last Modified: Wed, 24 Jun 2026 23:04:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e708e75403cdf41df22579f7c35bdeb0ca563a60fab98a318ed501e4024ae49`  
		Last Modified: Wed, 24 Jun 2026 23:04:29 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:126315f7e2c36461cbe1d1aee737dd12a950c9a9c372684800e27cd4974db094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156e73e5612591d921913d9408454f6f617f6871076c1d632cdf3971b1cd3dc4`

```dockerfile
```

-	Layers:
	-	`sha256:0dbe406dae2e4708eaa862b970136ddc83e7cb77e23b64d4d42a408eb897ebe0`  
		Last Modified: Wed, 24 Jun 2026 23:04:35 GMT  
		Size: 3.8 MB (3792387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7b6514c9c636164f07c41f22a034292dff1f93cf7925df01f4458383767733`  
		Last Modified: Wed, 24 Jun 2026 23:04:34 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:90450ad3037e7293a2fc28f6012b12e62dd70ed2a019616a894d52da42f4142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215496129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743a372c258248c1ce061a2c4b3d5286b863508c0c74021939ae0fc3ff9049cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:45:18 GMT
ENV container oci
# Wed, 24 Jun 2026 06:45:18 GMT
COPY dir:0b29f9e66bf048f7202a79e2f728b8f136d2a972d39ff75508b0f9653d433ed0 in /      
# Wed, 24 Jun 2026 06:45:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:45:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:45:19 GMT
COPY dir:1852be49c9caac8615951d68388d7f8791140b539cc11bfda91b044119d75a5d in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:45:19 GMT
COPY dir:1852be49c9caac8615951d68388d7f8791140b539cc11bfda91b044119d75a5d in /root/buildinfo/      
# Wed, 24 Jun 2026 06:45:19 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:44:57Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:44:57Z" "architecture"="aarch64" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:44:57Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:03:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:03:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:03:25 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 24 Jun 2026 23:03:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:03:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:03:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:03:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:03:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6bcf33c78aa091990500f016c1ed0cb35bc3f67461b918afc9de35f0b601382c`  
		Last Modified: Wed, 24 Jun 2026 09:11:21 GMT  
		Size: 33.0 MB (33046417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8526ab18fae995e3ae9ca52e4f07d007c4b86b7515e8e7de60c39f057c7a75`  
		Last Modified: Wed, 24 Jun 2026 23:03:51 GMT  
		Size: 37.7 MB (37712409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cce1fd714f93551c560b4ba8465df9dffb9e97d0d6b9bba617187fabf990ac`  
		Last Modified: Wed, 24 Jun 2026 23:03:54 GMT  
		Size: 144.7 MB (144734889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac3d0714cd87502820c1334cf844e98a1680e57cc2c8a8f8b136ee90c370fe1`  
		Last Modified: Wed, 24 Jun 2026 23:03:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6193964866e007f6beaeec8e1605fa0b46a0c5dab3ac21f4142c26aa83330be6`  
		Last Modified: Wed, 24 Jun 2026 23:03:50 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:23cf40339a534ec9faa0f0feb6dcfd4a2808521fca6b8af307f7724d960be28a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efa2052b3ec715eda18c6123c0be7e344d647eb4c4fe8b25848e4cde89c3cdb`

```dockerfile
```

-	Layers:
	-	`sha256:dc9a05cf7b2587654db37d3e2d903240a51e2dd00be13cbb646beee16a238e83`  
		Last Modified: Wed, 24 Jun 2026 23:03:50 GMT  
		Size: 3.8 MB (3791813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a4d636cfd67651ec6ea50e50015eb6ffd4e9e5a0715a1ff1af7e37dad2062a`  
		Last Modified: Wed, 24 Jun 2026 23:03:50 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:94a951cf17b11d311f287768215c55cb1dd3381f9516173d806a86c68a42b746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224322455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122840c9979d070258ffbb28ec5ed1f8d16dbfe54c89b9251d3e8d79443a4d3b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:45:06 GMT
ENV container oci
# Wed, 24 Jun 2026 06:45:06 GMT
COPY dir:edae26e2804200dda741354aeaa508164e0f6589abbc418ddf0174c7e9c74460 in /      
# Wed, 24 Jun 2026 06:45:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:45:06 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:45:06 GMT
COPY dir:4159190efbf3bf817f31486123f361d6a5105b0e524913dcf5088003851d564d in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:45:06 GMT
COPY dir:4159190efbf3bf817f31486123f361d6a5105b0e524913dcf5088003851d564d in /root/buildinfo/      
# Wed, 24 Jun 2026 06:45:07 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:44:49Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:44:49Z" "architecture"="ppc64le" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:44:49Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:02:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:02:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:02:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:02:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:02:02 GMT
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
	-	`sha256:c0e83bd19bb537d0b48ac2365b13cdff44e889f5083fbf4be3569d1b4825377d`  
		Last Modified: Wed, 24 Jun 2026 12:17:52 GMT  
		Size: 39.0 MB (39004054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86309525b0d7959e843b2d2b23c4513e7ab084fa30bba69cb7f4566f4379eb6`  
		Last Modified: Wed, 24 Jun 2026 23:02:38 GMT  
		Size: 39.5 MB (39527160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b4dca4b4efaf9004fe85577ee0703e4d0b645fbb127e57ba89f0256cf1ae2`  
		Last Modified: Wed, 24 Jun 2026 23:06:40 GMT  
		Size: 145.8 MB (145788820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb84942fb410750eed5a63348a98ef297c21d806976dbf7cd3f724bbee28e49`  
		Last Modified: Wed, 24 Jun 2026 23:06:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c9ce2b1b9368943d5e071dcbd79d8aa441c602f98de2d56aa411e9df5be80d`  
		Last Modified: Wed, 24 Jun 2026 23:06:37 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0c173b1023b08ee0a65131fd3095d8e1a517ca4e7bca3a5f9e399dd4cdfcffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1b011d0c0021f66e6d6cf6fc269196e9f8d3f80317792a95d240c5f28f5c35`

```dockerfile
```

-	Layers:
	-	`sha256:b352ed04a7f1c9fae59fec7132d7940d30406ef7d6ac19beb545e6f4d40db352`  
		Last Modified: Wed, 24 Jun 2026 23:06:37 GMT  
		Size: 3.8 MB (3779219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1abd190d35203829c918f18593755383b9892b8efede69ead15544bd682d43d`  
		Last Modified: Wed, 24 Jun 2026 23:06:37 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b6f42d3930e870940c1d12ff760a3df17398c394d3d7916e88af49e52e379bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208840056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf2971ebdd2ddd4a7749d2c49700e31f075fcd5730a5b4db70d285ac239ac40`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:50:01 GMT
ENV container oci
# Wed, 24 Jun 2026 06:50:02 GMT
COPY dir:44a98658e38dbd3fe1a481ca6dd5239f51de526a3f13e8e4aae2600c0e195400 in /      
# Wed, 24 Jun 2026 06:50:02 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:50:02 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:50:02 GMT
COPY dir:faeaf738fafa5618598acb30c3f03d041d09c185c5e2d603c791711084b47697 in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:50:02 GMT
COPY dir:faeaf738fafa5618598acb30c3f03d041d09c185c5e2d603c791711084b47697 in /root/buildinfo/      
# Wed, 24 Jun 2026 06:50:02 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:48:38Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:48:38Z" "architecture"="s390x" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:48:38Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:01:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:58 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 24 Jun 2026 23:02:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:02:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:02:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:02:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:02:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f8130189e85e92c4ff7cc258627f77e071b689832e41f79f26767374d60fb4c3`  
		Last Modified: Wed, 24 Jun 2026 12:17:47 GMT  
		Size: 34.8 MB (34775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e258a83fe70f2f168f5b4f2b3184cba856f596dee52b05bdf5b1eb5bfdc3d32`  
		Last Modified: Wed, 24 Jun 2026 23:02:28 GMT  
		Size: 38.2 MB (38150217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e73346d46ece79e5c7fee8d21d5fade7d04eed0d650039efc19457fae62b0`  
		Last Modified: Wed, 24 Jun 2026 23:02:58 GMT  
		Size: 135.9 MB (135912330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977c5c2c69d6bc11e295f01b15cc9484c57a3ad8f66645f73aa45b0ab2a33a6b`  
		Last Modified: Wed, 24 Jun 2026 23:02:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c51ee5f1a4a6635ac6c56c1b40031278f8a8ed7d8e7d33b1d6de85870291f9c`  
		Last Modified: Wed, 24 Jun 2026 23:02:55 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1b7118c6fa59b160960bf3ad186cadab9f6e98d768ccdbac794d0e516461eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d298d4dbc8e4ba16f374c27f5d16bf4b5e1a8b314a6623309449831605c36e87`

```dockerfile
```

-	Layers:
	-	`sha256:99022e146345a01be8b14e614b660f7f4a46e7136005884cc19ba04336bc9dbc`  
		Last Modified: Wed, 24 Jun 2026 23:02:55 GMT  
		Size: 3.8 MB (3777977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2620da606c9e3d84dc7d393ec793b42c85dd6a87ad7d7afc2a212047afac9ccb`  
		Last Modified: Wed, 24 Jun 2026 23:02:55 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
