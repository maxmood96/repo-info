## `eclipse-temurin:21-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:511b801c4c7ff0b7eb895f9d2f934e967bf5a8f226f5ef2d023d7e6c687e7aea
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

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b005898cb5e007fa223989c7cc8b9703a666b0039ecb58833bd4ee9c76ce001d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246399025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939506787cb9d9114fbdd5e3fc33731d414d29f3b7efb5a07f23591814ad6101`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:d7d46744a920e661eed10a42e2080d8056941b338e371ab560c4c2eee7e7a070 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:2c9300aa2a82321bdb1295eb5cf59270c200f77d73b01c9b866932f5e4bf93c1 in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:00:12" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fe33f3d694b6e20455a988c4bdb920e5a216d54c81a4c79494b6d0debd58f76f`  
		Last Modified: Fri, 08 Aug 2025 00:12:36 GMT  
		Size: 33.5 MB (33498072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9c7ba9eb9f4740398a9c33b39e2241114c8f5b8d2f93c4bc855612f0825477`  
		Last Modified: Wed, 13 Aug 2025 23:02:43 GMT  
		Size: 55.1 MB (55090945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab1c18d37460483a2a66af4e27268a71b8c57063e6a7d69162509ff7a62fd36`  
		Last Modified: Thu, 14 Aug 2025 02:01:05 GMT  
		Size: 157.8 MB (157807587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ffc1f481884f023517130c0bab0cd8cb8fe9169ca985b95bb8348edb96903f`  
		Last Modified: Wed, 13 Aug 2025 23:02:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b932c22d03b1960f4a887e7d1404c143a98aae01fb72d6142d7fa1fc2f2891`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:527216e0865de8bae2a1c6ad532d1362b8e1be2b7bb28977c788c2c9562ebebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5698384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920ceec66fc6ab71daac63a4105003bd41490ac13e47035d5572c51ef4ee960b`

```dockerfile
```

-	Layers:
	-	`sha256:e1e1d579d22f8defbba9d2bea4ac2e191d2bf9683db5b3893acc09d49c288125`  
		Last Modified: Thu, 14 Aug 2025 00:14:42 GMT  
		Size: 5.7 MB (5677049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509aa2f0a1b4c2e54e59afcaff900892556868a193166c434e50cfd8bf52f391`  
		Last Modified: Thu, 14 Aug 2025 00:14:43 GMT  
		Size: 21.3 KB (21335 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:92e71a27c4470dcd826a7d22071dd314e131d43f46b5864b476bd5620616e0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242496434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d43281b020d0e4232fa7762a148ced4f4eec77e38cafdb39afce1bef0ebf4eb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:8385fc5490591ca16c81e8d24d20265b9384f30798583b224537cb1d56b1a850 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:06:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ed98dc7fc2264d2da8c020e12ea4548801fafd192d4c74444ac087ada4c6d75`  
		Last Modified: Fri, 08 Aug 2025 00:12:34 GMT  
		Size: 31.5 MB (31546088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0156aa0baa8f8522aa7e2a1820c735e597ad956ddf096f06ab53a2967160bae`  
		Last Modified: Thu, 14 Aug 2025 10:11:05 GMT  
		Size: 54.9 MB (54863066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56511dd767eb26e11f35267e8a2d9aa00a20f7c3bf17fb745d406b8df8f3d73f`  
		Last Modified: Thu, 14 Aug 2025 10:11:17 GMT  
		Size: 156.1 MB (156084858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc0d015ac098a499a7e8118e3a030220dbe3b459d215144d217dd87df811349`  
		Last Modified: Thu, 14 Aug 2025 09:15:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1905a0fb39eda0cbf6cb6a159c233e87ac4cd0d4bbd1370a31cdf8e70c46b7b5`  
		Last Modified: Thu, 14 Aug 2025 09:15:30 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:54614770978e4bdac3f8a3b8b0e5e7c49d57c7fbb0c5125d692bf320e5c6c887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5697990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b140994714fdf0afdcb8f1f6a76677fc32ce7ba2446ec129623f983d77c69b4`

```dockerfile
```

-	Layers:
	-	`sha256:dd3302e38dfa8912bf28e989bcee69b4079aa60cfa9245cd89033f08f981bb95`  
		Last Modified: Thu, 14 Aug 2025 12:14:52 GMT  
		Size: 5.7 MB (5676539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7868b165bf57a617357953ff13fc8172fb1e0ecdb48d7dac68a043dd77f1c0`  
		Last Modified: Thu, 14 Aug 2025 12:14:53 GMT  
		Size: 21.5 KB (21451 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:a6fbe5a5aabd95870543de4d7ccf1825d59fb942b4411e8e2867fd8f1979e236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251878475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb7ca7d89533a21fb0b65847dd9e4fd716c22493a63aa5f17740d7574ca3a97`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:640e0e573d0fea25191602587d27a678361464a59a51c46e7e2ad55c65a20739 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:14:08" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fbda37dec747d2d48a0b731bbc4647a80d0ad38995d3e592715932bca71e095c`  
		Last Modified: Fri, 08 Aug 2025 00:12:35 GMT  
		Size: 36.8 MB (36811145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624c78cc03453e81963d16cbd8cf44b57233f3676f5c0b5a6ae9b680b7e1aca3`  
		Last Modified: Thu, 14 Aug 2025 04:45:35 GMT  
		Size: 57.1 MB (57099241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678d81e337fb7e19b928482290f04504f0be4ab44154ade3ba4c1ffe91a46a12`  
		Last Modified: Thu, 14 Aug 2025 07:15:36 GMT  
		Size: 158.0 MB (157965668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe27f7a9bbdf4dfce1af9ede0d86513900f19403b506c98dddce6a11f23a1348`  
		Last Modified: Thu, 14 Aug 2025 04:57:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47d89c34ce33ed642334284e79e48543e23c41516dc269e30a30ffc856c66a3`  
		Last Modified: Thu, 14 Aug 2025 04:57:50 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:03634f3a07bffce40f98c1fa084af2fed52c88146c24c2b95164430f82b12083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5685572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2f36635007bb15c400c2a7b13462ffa2f08cd9bd8ca8e057a45911194190ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1b47dd5b58c5107ca47ff8cd36c28400494a59f42d1b047d163ceb319a0c48e`  
		Last Modified: Thu, 14 Aug 2025 06:15:05 GMT  
		Size: 5.7 MB (5664201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80578fee172f3dc8a3dee0683d7581db5dbfdc6f2fbd9ec11e1fe766060586d1`  
		Last Modified: Thu, 14 Aug 2025 06:15:05 GMT  
		Size: 21.4 KB (21371 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:005131d5c72b7b5e39ae7b3bc7f390b0da3f648d02fb33d3881a23fae312231d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236114135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78922702e60a5714bdb15c8e46259ad0c45ddc0038a24ede407292c2d1728ba3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:bb8541e617ae72e609facfec80e743cc4f049732f5a1f4acff90ff475615b5e7 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T19:09:07" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84d3bdaa36c0d56559b106975b26dde8bdf88341585cb0bf151bc1ac5c802c23`  
		Last Modified: Fri, 08 Aug 2025 00:12:36 GMT  
		Size: 33.4 MB (33411761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4608aad02821a2c4ed1f8242350611f4dd6e9c2061ab67d2b52b6786fc2bc728`  
		Last Modified: Thu, 14 Aug 2025 03:59:46 GMT  
		Size: 55.7 MB (55673689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff02519f665e7b6d4b9045f403af2af566c4b0d4b96c390d4a7de2b3f7532237`  
		Last Modified: Thu, 14 Aug 2025 07:15:33 GMT  
		Size: 147.0 MB (147026267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809f001dfe637d6559bf744613680b88fd70b22a9109e4084fe6c47f21240de`  
		Last Modified: Thu, 14 Aug 2025 04:05:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6709d94c8533cc74bb2f8223db0c15ef6888029c67ed102bcb5e1ac422cd7539`  
		Last Modified: Thu, 14 Aug 2025 04:05:37 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:864640702a828b55e9ccb80915e23c2aa39a69efdc7d49f9b216fe026628e1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db0634c1d28fc37484d1711be635d96ac94d185158c0a843e4f8c12c899bb31`

```dockerfile
```

-	Layers:
	-	`sha256:d3e136c8ec2472c4d2662295aecbb9606b1726a436f532d4c89e0fc9bba8122d`  
		Last Modified: Thu, 14 Aug 2025 06:15:10 GMT  
		Size: 5.7 MB (5662575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdef9ca53e1816923cbcb480b5be2b8b4989d88844f858948130f806a7c949c`  
		Last Modified: Thu, 14 Aug 2025 06:15:11 GMT  
		Size: 21.3 KB (21334 bytes)  
		MIME: application/vnd.in-toto+json
