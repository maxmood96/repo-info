## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:092b9b82682d40e671c27016d598cf658173d8d96dc28dda3aa3aa4416f8a1c7
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

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fe6acfa6c6ce4b50ddb9287eb7ef37f8136547cfc2cc7117b923d03ac9f9cd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212649048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab49db2c7e792ca0bed9042666e962c721aa4b3bbbb471e026619c4f92ace7f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:47:05 GMT
ENV container oci
# Mon, 20 Apr 2026 00:47:06 GMT
COPY dir:95d17c57ef40a5dba79704e92b9c5527d3acb3226364e42c0d41763471e61ce6 in /      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:47:06 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:46:48Z" "org.opencontainers.image.created"="2026-04-20T00:46:48Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:46:48Z
# Mon, 20 Apr 2026 23:06:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:06:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:06:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:06:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:06:18 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 20 Apr 2026 23:06:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:06:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:06:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:06:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caecb4e30e48b94915c873b145eb5d277a1098fd069faec96c54548af92ba81`  
		Last Modified: Mon, 20 Apr 2026 23:06:43 GMT  
		Size: 30.4 MB (30367028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364c7c3725266e68c5c939a6fb4d4e41a86c75b0ee5c46fb4948ab87b3f1ec04`  
		Last Modified: Mon, 20 Apr 2026 23:06:45 GMT  
		Size: 142.3 MB (142263307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586ad9b7cd7fccf6208b0b9fe9522fa1c6bb0e8b1ec534a033f9eed8e0ace92c`  
		Last Modified: Mon, 20 Apr 2026 23:06:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d53d194aac5335fcf01befb7c63265d445e9f04e2ed83a97dac2ae2b3e19913`  
		Last Modified: Mon, 20 Apr 2026 23:06:42 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bcfe57cd9cbf7942da19d5bfe218f174974537d9b7c9a76a2fba12430647a65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885eaae2bbbd23ae29b922430a5b1862c8b710b9a179470731b7bc58cd23d606`

```dockerfile
```

-	Layers:
	-	`sha256:05d07d091820160fe66553e148a4f5ac34cfc838991e19f4d53e81bbbf57b61a`  
		Last Modified: Mon, 20 Apr 2026 23:06:42 GMT  
		Size: 2.5 MB (2519706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72284edbf5ec7236219c2d9b0495a244ac020ea1589298f94fabfaed16821e7d`  
		Last Modified: Mon, 20 Apr 2026 23:06:41 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1fdbd9d5e57da21fae0ba0211fdb2a67c22dc1bb9b24d188287bd31ed321c866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207960256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f4fdb715584628a822d56dd32fcdb7a1593e5c81cb154336a472d098426aa8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:49:28 GMT
ENV container oci
# Mon, 20 Apr 2026 00:49:29 GMT
COPY dir:2db86b8c6d033296a751d728266ea755c08c1579f6b374a8f32773f7c153c4a3 in /      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:49:29 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:49:15Z" "org.opencontainers.image.created"="2026-04-20T00:49:15Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:49:15Z
# Mon, 20 Apr 2026 23:03:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:03:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:03:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:03:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:03:50 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 20 Apr 2026 23:03:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:03:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:03:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:03:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8debca61d243d998bf3bf52e935df4db45aecedd074c5f013abc40fd316c45f`  
		Last Modified: Mon, 20 Apr 2026 08:07:44 GMT  
		Size: 38.2 MB (38200123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e8524d809b2b5b49c68cc415c0bbc7f5f39037d4833e552ddf0cc7bba42251`  
		Last Modified: Mon, 20 Apr 2026 23:04:17 GMT  
		Size: 30.8 MB (30798016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb156bd516f447ad2f2589b7b0cc2f28ce3bb8b9a36cb11866d9bdfbfff0de0`  
		Last Modified: Mon, 20 Apr 2026 23:04:19 GMT  
		Size: 139.0 MB (138959697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a54b7dc858a7280d9603aec2783a65ba5a86ff3730e87596610272552aa38a`  
		Last Modified: Mon, 20 Apr 2026 23:04:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff5ab8e021609ac03d15b51dfb525b83a7e358c0b49a0913287e00e9f148d`  
		Last Modified: Mon, 20 Apr 2026 23:04:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7b60196cf8a2c77861fdeceecc532691d4810a9a23e108540699826b77cd2de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9928ab9f7518637e21a005b4320c03c73b2e34f989bad410bf7e48204f5ab768`

```dockerfile
```

-	Layers:
	-	`sha256:b69d79a0a574103a1968c3c31ca7fc6cf5a2b45b902c92b69ab4370c84462dc4`  
		Last Modified: Mon, 20 Apr 2026 23:04:15 GMT  
		Size: 2.5 MB (2519694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285d753436502154fef53845f8e73bb8a5b5ae20050415486a3755c5a6cceae6`  
		Last Modified: Mon, 20 Apr 2026 23:04:15 GMT  
		Size: 21.3 KB (21260 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:321956ed9f2e0b6e02f19fad1dafcd3bd323dbc5c68c72fda3370961187a92ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206793956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6481261ff5a13a4c88b73e803855f3a9e4ce91b3281aec942b03dcb8e8457f57`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:48:23 GMT
ENV container oci
# Mon, 20 Apr 2026 00:48:24 GMT
COPY dir:8240d23726e865ba51f291ba4ea188782a75a0af67ec349dc8d9d3bc145ecd05 in /      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:48:24 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:54c55160da8e94b0ed06988eaccac768df07b2ab8418806d9245b992ab4c1444 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:54c55160da8e94b0ed06988eaccac768df07b2ab8418806d9245b992ab4c1444 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:48:13Z" "org.opencontainers.image.created"="2026-04-20T00:48:13Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:48:13Z
# Mon, 20 Apr 2026 23:00:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:00:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:00:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:00:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:00:52 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 20 Apr 2026 23:02:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:02:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:02:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:02:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d0996bd7c74d1634fd0ba1753a8f74e86b97c5b41318f888d6b7bcc768131db`  
		Last Modified: Mon, 20 Apr 2026 12:13:59 GMT  
		Size: 44.4 MB (44443917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b1bfcc64f23f4a2cc6ba069104831d0f144abd63cec2aa7e370ca093096b9`  
		Last Modified: Mon, 20 Apr 2026 23:01:35 GMT  
		Size: 32.8 MB (32848454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa334dff8c9830c244ed51c7ab108cd6aa3297f2f121ba15cea51e261150a66`  
		Last Modified: Mon, 20 Apr 2026 23:03:24 GMT  
		Size: 129.5 MB (129499166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a57890c3ba244cf14ef3b31e590839753ac4fe19ac2d300fcce3b6af5ea55dc`  
		Last Modified: Mon, 20 Apr 2026 23:03:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7f750da78a1ac77e561dba506646eee579fd31aa4405eabc57359125a43fa6`  
		Last Modified: Mon, 20 Apr 2026 23:03:21 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:19e61a2dbfd84ca9b48c3951606df78af29d4b1bd00335124b9d4d0949e41d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e762772000a55ffba9379cd048d5bed69b94db02746aee3a8f268fb82a91ced2`

```dockerfile
```

-	Layers:
	-	`sha256:d382b71f867789c5eece296a23dcadfe699087e90d7e1cd1945b568fa3b455c8`  
		Last Modified: Mon, 20 Apr 2026 23:03:21 GMT  
		Size: 2.5 MB (2517183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8ade8d15c6d1e27e34b54371b2dff12dfb3af2e965654f7e2ba4bfa0eed060`  
		Last Modified: Mon, 20 Apr 2026 23:03:21 GMT  
		Size: 21.2 KB (21179 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:52c95d30d8c87c6b48e0585d3ddf36de1262d1e4a94870915f5676c05f4e263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191478699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54c2b9ce0e0425f3d1f5d7343e8600f0b8255636572083a6d2709122ea2d033`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:51:15 GMT
ENV container oci
# Mon, 20 Apr 2026 00:51:15 GMT
COPY dir:b4a1afe8106f1085d0935fb4f5d1d721db68a582913c2d55b2d9aaa1600bd93e in /      
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:51:16 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:3dec04e5e5d89154231655b5548184917b8c190a374813ff448dab4392492998 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:3dec04e5e5d89154231655b5548184917b8c190a374813ff448dab4392492998 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:51:16 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:51:04Z" "org.opencontainers.image.created"="2026-04-20T00:51:04Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:51:04Z
# Mon, 20 Apr 2026 23:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:04:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:26 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 20 Apr 2026 23:04:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:04:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:05:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:05:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:05:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32c0d17b4c811788343ca79dbd73a2cbd36ad958598e189725c863447313e0d3`  
		Last Modified: Mon, 20 Apr 2026 12:13:49 GMT  
		Size: 38.1 MB (38114922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd300f82eb1e8ecf5492fb727d38ad64a99b25f79e39a70bc453a3b2d46ba5a7`  
		Last Modified: Mon, 20 Apr 2026 23:06:58 GMT  
		Size: 30.4 MB (30388716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d108d761ce877ef2ce4fc13f7f6ac94beebd51c02d9d10a272f8598d77699e`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 123.0 MB (122972642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0196e5aa96cf50ca6b6eb49961ca7b50b91d44c73a8688be8fdd80ce605b662e`  
		Last Modified: Mon, 20 Apr 2026 23:06:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0168cbc2d01687f4d2edf2366249394b570042cd08e3238f61174107264007f2`  
		Last Modified: Mon, 20 Apr 2026 23:06:49 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4d3c0c111c2b5ee56901fcae590d402869de47b4f08b25c6e039fefbd9eb5fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb4ecf7beb92ea3aedac405ad34998692a5b733fd7936b4dfbbf61f9330cba4`

```dockerfile
```

-	Layers:
	-	`sha256:2685fd83552c6ac555cfcac83cf2b0c075af7d5bff7634fb24dfa47d93ca30e8`  
		Last Modified: Mon, 20 Apr 2026 23:06:51 GMT  
		Size: 2.5 MB (2507102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41fa3a796ffa2c6f7618e34fb06732a3b3fbe91d2c94d80ba6dcfc044199d323`  
		Last Modified: Mon, 20 Apr 2026 23:06:48 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json
