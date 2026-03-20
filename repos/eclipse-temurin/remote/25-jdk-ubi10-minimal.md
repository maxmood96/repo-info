## `eclipse-temurin:25-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:0025a03a233edf1294a7a025165b0ceae6aa6d4da64662e1a123a7360776a3c9
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

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6610ab11f95ad9e41f47ad9581202d59a2ffef03c2f077f666c6c3bde0a3801e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164318214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc948310885425539fb884f345d0c3f6dcf5dd388cf0d36e04c6dc3411ec2255`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:53:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:53:01 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:53:01 GMT
ENV container oci
# Thu, 19 Mar 2026 04:53:01 GMT
COPY dir:af440ed069b945cf125ef868e769f70d1b1e33071b111d96c1e9a1ffc5f76e4e in /      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:53:01 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:6585c86973269b2041af40b485e0e6f045b49959f72c04fee4a05795e2e5a97c in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:53:02 GMT
COPY file:6585c86973269b2041af40b485e0e6f045b49959f72c04fee4a05795e2e5a97c in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:53:02 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:52:47Z" "org.opencontainers.image.created"="2026-03-19T04:52:47Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:52:47Z
# Fri, 20 Mar 2026 00:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:17:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:17:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:17:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:17:24 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 20 Mar 2026 00:17:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:17:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:17:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:17:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:17:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f862e22eed3c55bcf45baceaa7dd39dbd424275e0f2d3130583784c94e488dfd`  
		Last Modified: Thu, 19 Mar 2026 06:14:45 GMT  
		Size: 34.6 MB (34610902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c04fcb3cefc56b5fa03c76ff01b2b9df689b3b272c4e364903f16ce68fd9d37`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 37.4 MB (37446929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6713951577462f6197446adfaf2cd004c214b7017c3b6c522a5d611576475dab`  
		Last Modified: Fri, 20 Mar 2026 00:18:14 GMT  
		Size: 92.3 MB (92257965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4413150d64d2a1b5c73615df91697080d17af836e682b17ca733c463bd988`  
		Last Modified: Fri, 20 Mar 2026 00:18:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fa8336613eb9e021af5b3f282cc46cdc62253859733e27b29ee43192693f10`  
		Last Modified: Fri, 20 Mar 2026 00:18:11 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1f36e43ed659a12c52c02e28c7c4169a0742126c7c0f2012f5ee802c367a50a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3778484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7136c5682540caa51c3fbbd90e4de5be07fc4ffa090cfed7f17725bb5df8e0e0`

```dockerfile
```

-	Layers:
	-	`sha256:2ff4ea3e7646c96e2667f5c5089d6859c47d7cd3e2033b93efb5507019afb02a`  
		Last Modified: Fri, 20 Mar 2026 00:18:11 GMT  
		Size: 3.8 MB (3757171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053e2b8eabf72f0e38ca3dbaf089b7085f44eda4538609b3f748bc863696dfb`  
		Last Modified: Fri, 20 Mar 2026 00:18:11 GMT  
		Size: 21.3 KB (21313 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ed996c73b75b0b40806c8dfb4f01e3d09f53e548ad8430ae436786e7c196d0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161366577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a886a849ddddc82623e15aa87661ef8802074955c973362aab70a7e242cd9710`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:55:27 GMT
ENV container oci
# Thu, 19 Mar 2026 04:55:27 GMT
COPY dir:ddf23ac9073f2f0aebc549dd652158e51758019b3f147b69bcf85b8c51fd9394 in /      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:55:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:3038f4da402f5d3deadca7034502c693a744bf96305b10c79908db4a59bf74a2 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:3038f4da402f5d3deadca7034502c693a744bf96305b10c79908db4a59bf74a2 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:55:28 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:55:11Z" "org.opencontainers.image.created"="2026-03-19T04:55:11Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:55:11Z
# Fri, 20 Mar 2026 00:15:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:15:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:15:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:15:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:15:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 20 Mar 2026 00:15:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:15:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:15:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:15:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:15:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32559d11b9ee98b34627afd92e663006f6191d5024358c48c175361f14b3bf84`  
		Last Modified: Thu, 19 Mar 2026 06:26:47 GMT  
		Size: 32.7 MB (32683055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10fbcf144660556c5a7344ab4608530851325a049c81d215ba3760221cee3b5`  
		Last Modified: Fri, 20 Mar 2026 00:15:29 GMT  
		Size: 37.4 MB (37383254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc214319c2abef0b7f026b91370bb31f92544c7b5eced36b6f62b3f6342b43d5`  
		Last Modified: Fri, 20 Mar 2026 00:15:30 GMT  
		Size: 91.3 MB (91297850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055672969b006d395f2c74ef0f6ecbb42054df25f6834ffe53c47d1032349f16`  
		Last Modified: Fri, 20 Mar 2026 00:15:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238f923118d46ff12e781385c6a25fe99cf4b0f593a80c25180d6f34983d3fa5`  
		Last Modified: Fri, 20 Mar 2026 00:15:28 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1e0b339539d34a3c0c2a84933d716107f91ee0f05bb8fa54d4fea7a61caf049b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3778023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa796a08b9f5f6ab2c45f580b71877b0a0deb1286917a04c815d2cdbc3c5a473`

```dockerfile
```

-	Layers:
	-	`sha256:9f97d584fbf9e9fccaf8e19ea73685469da7803a07d4f6d9acc18760eb4dd627`  
		Last Modified: Fri, 20 Mar 2026 00:15:28 GMT  
		Size: 3.8 MB (3756594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf47a3f467e4fb9bb2f869018996389497b3bc9e49bc036df15f5ab94652fd0`  
		Last Modified: Fri, 20 Mar 2026 00:15:28 GMT  
		Size: 21.4 KB (21429 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:507cbad01bc1f3ea1ee164a8ea8b8b357f536ba1fc8acbf566f9b787b37947c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169569644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979d78ef2e97e294c855739dc9663fa8360219b7c4c1eb573aa0ee3ca172c252`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:54:26 GMT
ENV container oci
# Thu, 19 Mar 2026 04:54:27 GMT
COPY dir:02874e9a4cbd11d21ae5a0b0d5ceabca448e8e4b7d87ed83fe20e3fe3891053a in /      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:54:27 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:cd93def3bf43c5dabe55bff87f8d330823b7a378238d571cd76fa53ae8fb0d3c in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:cd93def3bf43c5dabe55bff87f8d330823b7a378238d571cd76fa53ae8fb0d3c in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:54:28 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:54:15Z" "org.opencontainers.image.created"="2026-03-19T04:54:15Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:54:15Z
# Fri, 20 Mar 2026 00:02:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:02:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:02:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:02:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:02:04 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 20 Mar 2026 00:10:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:10:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:10:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:10:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d4c7683a582dd524d9a529f07d62fb8d8a6768403c45eb8da73d739aaacbbd8e`  
		Last Modified: Thu, 19 Mar 2026 06:27:21 GMT  
		Size: 38.7 MB (38730914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cb46297f5b33cc4db0990c621afa3066c8a88767766b1d83c47221837e903b`  
		Last Modified: Fri, 20 Mar 2026 00:02:45 GMT  
		Size: 39.2 MB (39201421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328398164b8913ecb2b16547ea61e11d8ce6c0d80567a7051156e941bb03194`  
		Last Modified: Fri, 20 Mar 2026 00:10:45 GMT  
		Size: 91.6 MB (91634888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f551f87074551bd32528a8adc16932c978553c1bd961ddd304af422cd6c1589e`  
		Last Modified: Fri, 20 Mar 2026 00:10:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d523cf40311a087d77797706582123633e3dfe4be351705ecff49d4ea8894c`  
		Last Modified: Fri, 20 Mar 2026 00:10:42 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:68f95bdc8250abfe38a25daec7379a6e5310ee96b55468385d949d602fe0d83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1d457ebddc2582224d48a2fc0e7c2dd5d3bbda1dda657c963ac27d53542857`

```dockerfile
```

-	Layers:
	-	`sha256:6ad9d4b128eb6c561892e8adf71fc4b52c0a4c6b9462f465e81616dbaaedc992`  
		Last Modified: Fri, 20 Mar 2026 00:10:43 GMT  
		Size: 3.7 MB (3727315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab65a47cdc85c1b9fb83619944de3cd3f20bc268420249196fd70e79df8c1c4`  
		Last Modified: Fri, 20 Mar 2026 00:10:42 GMT  
		Size: 21.3 KB (21348 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:5de7c1de88acb30096ac16b0fddc4cd18b8a090d8ba0a860a216fac5bcc6de78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160453981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cf1b04ed5b495be3639a8e3b110945ea0f5fbb855af67ae6215f7028da514e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 05:27:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 05:27:34 GMT
ENV container oci
# Thu, 19 Mar 2026 05:27:34 GMT
COPY dir:f746ef018dd3f7fba95b363c4653a5edbac791b1963bab35d68387e37854182c in /      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 05:27:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:ccda15be012570b9ee4c334e02edf875ddce34b3e788c2b4b2da3a4753faf610 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:ccda15be012570b9ee4c334e02edf875ddce34b3e788c2b4b2da3a4753faf610 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 05:27:35 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T05:26:51Z" "org.opencontainers.image.created"="2026-03-19T05:26:51Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T05:26:51Z
# Fri, 20 Mar 2026 00:01:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:01:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:01:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:01:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:01:45 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 20 Mar 2026 00:04:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:04:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:04:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:04:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:04:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63c8858510565f2c5ca6837c562373228e6bd18c78642693e77e10422f59c586`  
		Last Modified: Thu, 19 Mar 2026 06:26:56 GMT  
		Size: 34.4 MB (34389317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52932ad68498d79edf7e415e512c223a0be61689d7a86e4d8782695524e4ae0`  
		Last Modified: Fri, 20 Mar 2026 00:02:12 GMT  
		Size: 37.8 MB (37826887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c16edf619fe70831825402cbde19e2a7dc0592e0f47403b3e523deba57a8ea6`  
		Last Modified: Fri, 20 Mar 2026 00:04:42 GMT  
		Size: 88.2 MB (88235358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a535e63e6f79160fedf6a86eb2df4978a44396f4ec9e1ec31bb7497bdffd747`  
		Last Modified: Fri, 20 Mar 2026 00:04:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd746a19bbb3eaca3ed80a259130dacb3e158b414a0e7226c01e91652ce12d3`  
		Last Modified: Fri, 20 Mar 2026 00:04:34 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a0a7d383f74b23e24dd50eb04e53098c3cb949966f3cc9e88162a5393a228d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecff9779365dbe06f878c41b513927b098b0d0ae7ae84be87402deb19042d24`

```dockerfile
```

-	Layers:
	-	`sha256:f3851e76bc43259b8ba1a20538f8e64b73ba5dc42958f1a34434c60aadc5ea13`  
		Last Modified: Fri, 20 Mar 2026 00:04:40 GMT  
		Size: 3.7 MB (3727323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:012256fcf06d9137b95958bbaf442b4249980c7fb26f5662bf997c521f1bb112`  
		Last Modified: Fri, 20 Mar 2026 00:04:40 GMT  
		Size: 21.3 KB (21313 bytes)  
		MIME: application/vnd.in-toto+json
