## `eclipse-temurin:8-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:fdd43af42c44d5967aa70e65a7c2ddf1f88cd56a02008fb218b48eb8b98e04d6
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
$ docker pull eclipse-temurin@sha256:2dd9848fd73ef179c39412576540bf724de5cc74343f8e2302c95b00c552bafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129510309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0b5c76f45476e639f9c0f55c866e0af9c5e8419f2fa699c8cf2b53677b256c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Wed, 28 Jan 2026 19:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 19:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 19:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 19:01:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 19:01:09 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 19:01:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 28 Jan 2026 19:01:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 19:01:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 19:01:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6af7d70117fb54a1c19fa7ab0dd6387be5ab897497b2986acffbb49ebe56b290`  
		Last Modified: Tue, 27 Jan 2026 17:15:27 GMT  
		Size: 34.6 MB (34556452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07c4b90ad1632b62807fa00118e5bba9f56eab391acf26fe0b078e2f530e69d`  
		Last Modified: Wed, 28 Jan 2026 19:01:29 GMT  
		Size: 40.2 MB (40217484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a744026d072c972da34d2436a7a61b9dce3fc4851b0953ff91c1597675fe8d`  
		Last Modified: Wed, 28 Jan 2026 19:01:29 GMT  
		Size: 54.7 MB (54733930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7c504886105efce4b85c3f6df424aa74d77a4738f73c47dcd8fbf764a9a272`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abecee07dab24bf09b9ce0433c00d436a4cd2051227750acbad13b6db63c9023`  
		Last Modified: Wed, 28 Jan 2026 19:01:27 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3f94bb1d3f0ba96e65a698ac071cd0debc6d3b2560dde695d913847de3dae94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f9343802a359c20dc3e295587f5eb81c5c550cc8d446113d19bdb7ee14ba97`

```dockerfile
```

-	Layers:
	-	`sha256:24d51bf1bb0c8ba8f6d58dc4e71a23da42f805b78f25a115e0648a3d2612adb9`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 3.9 MB (3910065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2272b36fd0928d29e2e4575354fd01226ef17dfdabf2839a152460a96dac2b4`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ecd6af1a3d41d78c45f19ac99765b3ca88dd436692b4af3f715029629fa5fe23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126398370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf126e131ae19b28f3a1f474f0b12a3cd62aad0128ff2d1f648c6717e764921c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 19:16:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 28 Jan 2026 19:16:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 19:16:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 19:16:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:327940c40d800d56d0c471b5e46996d63f6fcaead646140bcef455acfb905b58`  
		Last Modified: Wed, 28 Jan 2026 19:16:48 GMT  
		Size: 53.8 MB (53815633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0604e5cbc76d6cff03984464cef1284363ea98eb9d525ec8490cf5245d68c61c`  
		Last Modified: Wed, 28 Jan 2026 19:16:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730eb3e2f26e85906f1bb556aa41be28d230888c6e882168bbf279c30e9d810c`  
		Last Modified: Wed, 28 Jan 2026 19:16:47 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8087b770c3b4f316e1ecb854f5ad0c6cae342ac4ec2da2ae00de3cf723e2f03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620fdb33bb0ce9763753467f5d7842e8371a42ce9bf93ffa75f5e82f25e97b84`

```dockerfile
```

-	Layers:
	-	`sha256:6ed61c4b92a7cef5aa685bb412b082bbf8096285bd6290bf6506b56928d6f0c2`  
		Last Modified: Wed, 28 Jan 2026 19:16:46 GMT  
		Size: 3.9 MB (3910189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6764f3ffafc98bcf44a1a392c67cc2c96830bfade88699a41ceb3150dde804`  
		Last Modified: Wed, 28 Jan 2026 19:16:45 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:32a39621d25df7d57fe5c8ae6ecc61eb9d5ec64d01cf934ae26b23bbc45bae1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129943350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ad31169760bd6ad3970ca645cfaff1b5b92214b5c38d1a8a58faceab69616f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 18:56:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:1ac303a5ec5cbd708079be3389cad6f8369d322977fa2cf328ca2ce7a4f9e544`  
		Last Modified: Wed, 28 Jan 2026 18:57:36 GMT  
		Size: 52.2 MB (52175831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56cb1d11c55c60279cbb4ed2dd82af7cfe415e9d281cd2fcd4833e2d31772be`  
		Last Modified: Wed, 28 Jan 2026 18:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c829aecc717a27dfe9d88271c2c658eef6d77f9892f710963d9f51c09f08b6`  
		Last Modified: Wed, 28 Jan 2026 18:57:34 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a6fe70628515b79f2783ddba8ea04266973de88327e9ee1c15124a19048b17f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c91b91d1535c94433c1a8377ae4924656e6ec00118f1b8d97393f9de87c959d`

```dockerfile
```

-	Layers:
	-	`sha256:df5a9cc62b646df15275efb0fa035b32b0c473f117d09b0d8670a2b9a4a59357`  
		Last Modified: Wed, 28 Jan 2026 18:57:33 GMT  
		Size: 3.9 MB (3897490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c5d294eaac6883418e0987f9c065bf94255b85ab405e865cce3d16232465c03`  
		Last Modified: Wed, 28 Jan 2026 18:57:33 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
