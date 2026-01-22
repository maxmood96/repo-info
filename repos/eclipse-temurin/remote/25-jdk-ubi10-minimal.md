## `eclipse-temurin:25-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:e405268ecb6939e1dc7f2a111b90ac05d8782198b8fa3b6b83f1f8947d06de4e
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
$ docker pull eclipse-temurin@sha256:f5bec124b868a9e5e6a1cc7bb754f232844a9e66f5f4127c4b68d887dd55e46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181906343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcd9f4ecfc44786ddf04bbfa826eedf2e128da14aefd5488be788078e4a72de`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 04:59:16 GMT
ENV container oci
# Thu, 18 Dec 2025 04:59:17 GMT
COPY dir:fdc8c39dddd7104eb139c404c8e963d7763f4f2dba800adb3cb1affa751115f3 in /      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 04:59:17 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T04:58:54Z" "org.opencontainers.image.created"="2025-12-18T04:58:54Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T04:58:54Z
# Thu, 18 Dec 2025 22:23:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:23:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:23:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:23:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:23:23 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 18 Dec 2025 22:24:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:24:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:24:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:24:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:24:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bbf656ece02bf42bcb72be26aaced8f9084f91250ae2336e1f2b7b9e8b979727`  
		Last Modified: Thu, 18 Dec 2025 11:19:29 GMT  
		Size: 34.5 MB (34531778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947fa77d92236d7708c9dd5127ac319d0dfb66ecb4d8c6da34db59d00d2f794`  
		Last Modified: Thu, 18 Dec 2025 22:23:47 GMT  
		Size: 55.3 MB (55325417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29338c551bc45d0bbf250592970f7b04a06889a5263de0b2a62b1de9786c0775`  
		Last Modified: Thu, 18 Dec 2025 22:24:23 GMT  
		Size: 92.0 MB (92046730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64918ffbe1fcb54b48c258b0d75f9770542176ba71715557ce5efac2eec3783`  
		Last Modified: Thu, 18 Dec 2025 22:24:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c96aca76843dfcf6ddcadb47924b43be94dbf7859b0ddf753420265a1270f`  
		Last Modified: Thu, 18 Dec 2025 22:24:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:16ef6e51e7e56b8f0e3639206471a38780208adabef7a035076e63c1991e8bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5652477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30cc5b24691a8b8348863f781beb8d1536dcc7a382707f470e068992591989e1`

```dockerfile
```

-	Layers:
	-	`sha256:3ae3852cf822745ab64e436156a103efc518b5446da2b37f05584abed989b746`  
		Last Modified: Fri, 19 Dec 2025 00:24:43 GMT  
		Size: 5.6 MB (5631188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49171ed9538db121fcd7be314200f45aef007afbe2f6420079b10c376195672`  
		Last Modified: Fri, 19 Dec 2025 00:24:44 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:21a7858664b40b448059c013ae173efb54c05c9e10a4d28e8cd40e7c0f13bc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178810993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3479cd2a8db9b49a47a8f54c9915fa28f5bae7c9b5f904511454b5650e4af67a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 05:04:19 GMT
ENV container oci
# Thu, 18 Dec 2025 05:04:20 GMT
COPY dir:04b750083472751a7f5154bb88e2ce4d0526c13f7486508dfd32af911f2d6c12 in /      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 05:04:20 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T05:03:56Z" "org.opencontainers.image.created"="2025-12-18T05:03:56Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T05:03:56Z
# Thu, 18 Dec 2025 22:30:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:30:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:30:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:30:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:30:46 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 18 Dec 2025 22:30:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:30:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:30:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:30:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:30:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f416e7c13e96a1bec342af3e79184aaf45de55dd66939245eb76ca02465c54c7`  
		Last Modified: Thu, 18 Dec 2025 12:14:26 GMT  
		Size: 32.6 MB (32633678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d948260fbeb5898b951608e82c62c396441948bd58cf3487ddc75bc89feaff`  
		Last Modified: Thu, 18 Dec 2025 22:31:15 GMT  
		Size: 55.1 MB (55118598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945294a41f01a860ee896a3ed13082b932d47912020e6b4d067b64862718e4d2`  
		Last Modified: Thu, 18 Dec 2025 22:31:16 GMT  
		Size: 91.1 MB (91056299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211de23a9661dc491541f18097deece8c7c0168be7865ed682032a65a678291c`  
		Last Modified: Thu, 18 Dec 2025 22:31:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454027df0d82c1aadeb9d60c48487b1013c0fbbe040fe8ea9e1e8de3ef5150a4`  
		Last Modified: Thu, 18 Dec 2025 22:31:21 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:17f5b45f15eb9cdb13a3f14df93c90411826a1e1aad5952f2eee80084c46bebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5652080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c07a69a2de00608b5cdbc1f74b20e50551866b32e9cde331522a62a9e6ca56`

```dockerfile
```

-	Layers:
	-	`sha256:31d94a42a792ec43434c94aedb5dd50dca78b3458e3058eb9bdcee86aefab5c2`  
		Last Modified: Fri, 19 Dec 2025 01:16:15 GMT  
		Size: 5.6 MB (5630675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bdb00507802d75b50358da97c5a0bfeea49185948add171ac8f5f58d873d226`  
		Last Modified: Fri, 19 Dec 2025 01:16:27 GMT  
		Size: 21.4 KB (21405 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d6bc07b489afd910ddb96b73e68c74772fe096bafced30333b6980c24fa7093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187647237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb1438088e7ee216deabb4cf90758534554cb1f8a98e602e450191db2b163a7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:03:44 GMT
ENV container oci
# Thu, 18 Dec 2025 07:03:45 GMT
COPY dir:530980282317924eec1c6623b725ebfc8622f7b70907079d2b485327f826b92a in /      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:03:45 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:03:33Z" "org.opencontainers.image.created"="2025-12-18T07:03:33Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:03:33Z
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:39:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:39:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 18 Dec 2025 22:44:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:44:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:44:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:44:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:44:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97de3b33554c63d2e40af1481c1da99bde18eb30eff5e4d230d8ec855811f50c`  
		Last Modified: Thu, 18 Dec 2025 12:14:36 GMT  
		Size: 38.7 MB (38688551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4559e7867acf4f05baf702a54db8a3e2cc5bd1a16c2dcecfa940d5c1ad1b6dfd`  
		Last Modified: Thu, 18 Dec 2025 22:40:05 GMT  
		Size: 57.3 MB (57343233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c901f5c99cf57502e858b5eee1e9cc8e9f0a5466c9e20cb195509a3bcbce3752`  
		Last Modified: Thu, 18 Dec 2025 22:44:55 GMT  
		Size: 91.6 MB (91613031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9272d59d36a69c550333e5d86a01e154f25e85274b5be59cd9c002913d038349`  
		Last Modified: Thu, 18 Dec 2025 22:45:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e080a7e257e17ddddc224c82b4261a30a07f093a8666045730d0d2fd4250839`  
		Last Modified: Thu, 18 Dec 2025 22:44:50 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:53bc0277fc137d7707bfab07985deb671483c456a334c82f65b751043d5e0329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5640963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c06ecd24e56a2688b8fb5633b7bc4978fd109830fca57b2cfe9e6e12bf97d71`

```dockerfile
```

-	Layers:
	-	`sha256:bff9d12119c52074f7d2b4007f34e2d8e0513b65dc8020e9d8a90018398380cf`  
		Last Modified: Fri, 19 Dec 2025 01:16:33 GMT  
		Size: 5.6 MB (5619638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b49cbaf4cb90b9b2959f85c2a9090e4b4b01f762df5c4fe15b305f458878f8e4`  
		Last Modified: Fri, 19 Dec 2025 01:16:34 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c1139844f2b799f0efc686b722665371c570483e18c50ad4095c3c5215945fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178475545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de59a1b28bf4674749b6ad4388c445a2495684e1e10d1576c3227b44eea188de`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:10:03 GMT
ENV container oci
# Thu, 18 Dec 2025 07:10:03 GMT
COPY dir:7d54469de7c29eaa832f7e98c75ae08842b7fae9314e66ea7e9e482c3966eeca in /      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:10:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:07:43Z" "org.opencontainers.image.created"="2025-12-18T07:07:43Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:07:43Z
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:41:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:41:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:41:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 18 Dec 2025 22:42:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:42:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:42:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:42:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:42:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:27a76ad55c4b879c1269027dfeec6783f235d82059544eeb7c62ecb7ad66011a`  
		Last Modified: Thu, 18 Dec 2025 12:14:31 GMT  
		Size: 34.3 MB (34340329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63f770e95bcd442fbd4b8fd68cccd7a912d2dd01d01bf876299e3b9c4b8eeda`  
		Last Modified: Thu, 18 Dec 2025 22:42:09 GMT  
		Size: 55.9 MB (55921082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a86798b558efb4d8d875a179c4db868f45fc2c6dea17a636ad8a351d068c96`  
		Last Modified: Thu, 18 Dec 2025 22:43:02 GMT  
		Size: 88.2 MB (88211716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf264ae291787a793a02fb55a8048dd9b401b80671dd4835b6ee5a717a4e3a0`  
		Last Modified: Thu, 18 Dec 2025 22:42:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22da806615f6d48dce6f9ae2432b30bd022d20e05181676062f89dd57706f466`  
		Last Modified: Thu, 18 Dec 2025 22:42:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b5df0fd1e97e1a94cb3ec32b1e7af2a0755bae17fccb7987fca3f15b72093ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5640551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ddc45d4d2945b132bf1fc44c918e52cec49202e69a4f8c4489533f63c0bb06`

```dockerfile
```

-	Layers:
	-	`sha256:a01690669757152ace2aede66e7e86ce33320bb55d4caa017962c84a17139636`  
		Last Modified: Thu, 18 Dec 2025 22:42:46 GMT  
		Size: 5.6 MB (5619262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ffae0c0f552d4c9d7e4b754433efb7e3f9290b1909e68ba5430726215983434`  
		Last Modified: Thu, 18 Dec 2025 22:42:46 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json
