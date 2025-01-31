## `eclipse-temurin:11-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:0862206b5fa9aee3194560a8a9c724a3c7435d62d9383669c5e35cb4ebaeabe7
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

### `eclipse-temurin:11-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5b5e5951d7c2e098e758dd8ad87c4e20a1f33b5616bb2d62e7cd11f65c6607db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218481192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5ffe183cd70df1a77209a64a6a037e98e8ec5a88e58b5b46ee611ab34483f4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff6a4bfa8adf5b14a65262624f4a3a245222169e132daf56c544376ee89030b`  
		Last Modified: Fri, 31 Jan 2025 01:30:14 GMT  
		Size: 37.0 MB (36987676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d152d4c50d5494c74b6eb2f65b783c6cbe1370013418d1548437305810031b`  
		Last Modified: Fri, 31 Jan 2025 01:30:15 GMT  
		Size: 142.1 MB (142058275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3be67b1c0a732bacd28d29d2a0722fe0e7667f6257f19ee4b06d11095e9893`  
		Last Modified: Fri, 31 Jan 2025 01:30:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eb62ffc4ba17b60ad94c8676ba31d9da56e7007d2094ec30f4e7161cc90815`  
		Last Modified: Fri, 31 Jan 2025 01:30:13 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a24d95684c8f3df01d1d4ef0aeb75964151275bc34850dea9982207ad3ae8106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3708024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ee4201287c6a036a33056b900ff2f6c2ef2141337049a77596bf0531875298`

```dockerfile
```

-	Layers:
	-	`sha256:77db333e5c9edf44878738d095667b4b751b92416dedc992829e9b533fe73210`  
		Last Modified: Fri, 31 Jan 2025 01:30:13 GMT  
		Size: 3.7 MB (3686310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade88fe41547fd746b1a3aea60aa9b709b143321aba0680f84dd96c80b799c09`  
		Last Modified: Fri, 31 Jan 2025 01:30:13 GMT  
		Size: 21.7 KB (21714 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c77190d56070fbbca907749c8f998b97bd55380f126740cba9e1b8de84fed34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213870402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4badd8d6ef718dceae4f6710e7fe3e8424c3c103bb8c2bd0d06b47c46c1498`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc249bdcd042886f9e42f55ca1acbc155028117c6226b2cd68dd2d0b94af56f`  
		Last Modified: Wed, 22 Jan 2025 20:54:17 GMT  
		Size: 37.4 MB (37443876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a079225fbd0f2910810798c4be9f68cf37da3d91c0f9b4aac174501d8fd5a9db`  
		Last Modified: Fri, 31 Jan 2025 01:37:24 GMT  
		Size: 138.8 MB (138846284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1234f10a044b15cde8290e1a01992642d9aecc17a29003adad612814733f780`  
		Last Modified: Fri, 31 Jan 2025 01:37:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c13cc7ff63f5e21677a42d04807da42724ff97c52ef8483a1b5db47d5e4e2f`  
		Last Modified: Fri, 31 Jan 2025 01:37:21 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:843621d404d7429152b6305de18f0a5836a5fd2940ff8d5dc122db28f1824299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfd872988d0aa6ce1f4780ae0238a88645a0ae30886fd90a9831302a693afda`

```dockerfile
```

-	Layers:
	-	`sha256:bc65bd76a90fae8ca4d370eba9c309531d142ab67811322a404b0b3d07d7602c`  
		Last Modified: Fri, 31 Jan 2025 01:37:21 GMT  
		Size: 3.7 MB (3686119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a86be7bd0e8b787a6341f2898bd82951101890349143faaabe471bb57364ca7`  
		Last Modified: Fri, 31 Jan 2025 01:37:21 GMT  
		Size: 21.8 KB (21831 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7be0fea958bea32006f11066f2adde7513198696b1f80c96aedf6bd21f2b3f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212563249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347e11965313433e96f68ca96501e11c02bf33dd5004713449022a7e88341d42`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:59 GMT
ENV container oci
# Thu, 09 Jan 2025 06:42:00 GMT
COPY dir:d7227f71d224f4a0ce6e41e096c5f35be3bfb0d1cc57d5e656694dcabcc752aa in / 
# Thu, 09 Jan 2025 06:42:00 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:42:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:42:00 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:42:01 GMT
LABEL "build-date"="2025-01-09T06:41:34" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:42:17 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dce878563f15050dbee433ee11b302dc91caccb7bbf30b63a4d16c18ac4571ad`  
		Last Modified: Thu, 09 Jan 2025 12:32:39 GMT  
		Size: 43.8 MB (43794360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e8d75484ae7e9cfff00aa310d4197973e5e690156a92349511c158be98059f`  
		Last Modified: Thu, 09 Jan 2025 12:32:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18197cf46ebd87e4c786c45f34ea15620d00514afdc79daf54b112ed798a5efc`  
		Last Modified: Sat, 11 Jan 2025 01:35:09 GMT  
		Size: 39.5 MB (39476434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba098b612851f5a6e61342a959d4ef276e90d303c466550d90f6d5fda2c137f`  
		Last Modified: Fri, 31 Jan 2025 01:41:33 GMT  
		Size: 129.3 MB (129289633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06ff3228101e6cdb850dbb5e2277a76e724a85240de84ff9f9504001f024408`  
		Last Modified: Fri, 31 Jan 2025 01:41:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf35be89cdb2f597a38487debdeea6c1e9f17f3ca09877d4db035f004d4bf20`  
		Last Modified: Fri, 31 Jan 2025 01:41:29 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9d3474bf9c4aa3209b02dfe8864e30dfe961677edbd76168302bb556b0605cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3705359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8aeba822925799878d46f8dc88c7920150f9ee464e8640a6a22e4e5ef5bbfd`

```dockerfile
```

-	Layers:
	-	`sha256:2dde586244ce0ce42d9d92dbdb6e322810a3b793d8c84b345731d35ceee23629`  
		Last Modified: Fri, 31 Jan 2025 01:41:30 GMT  
		Size: 3.7 MB (3683608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd0766b0d9c1f57c516779c07cfda9ab266dba24330dcc3d39e3aa3647b88bc`  
		Last Modified: Fri, 31 Jan 2025 01:41:29 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c6ae6ffa6d59d5981c6ba3fc9e7c648f04bd5ba086a50761b0e3ef175bc1848f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196521374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e463a0958bd980e761147cc84f34bc69c0c0b41687ff834589e801519cf5e9d7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:39:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:39:30 GMT
ENV container oci
# Thu, 09 Jan 2025 06:39:31 GMT
COPY dir:ac9a6f98f459f2b182d154b46dbecb42555c6dd9f1103593ad7ba35ef49f1c66 in / 
# Thu, 09 Jan 2025 06:39:31 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:39:31 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:39:31 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:39:31 GMT
LABEL "build-date"="2025-01-09T06:38:39" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:39:43 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8ee56b4600df35f4679f31d612bb546f04a8c0ff236484b5c24d4beec3d209ff`  
		Last Modified: Thu, 09 Jan 2025 12:32:33 GMT  
		Size: 37.5 MB (37533310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168fa7af747923a20c9ccecc35d6f8ea158b325819f175b7fbc3590d84656a8a`  
		Last Modified: Thu, 09 Jan 2025 12:32:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675f375cbacf7119aacbe8ef40ba25c801eee392e2f25776fea276c3252f817`  
		Last Modified: Sat, 11 Jan 2025 01:35:34 GMT  
		Size: 37.0 MB (37006874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e34661b017cf25765da525d96ab0a287a1c26b5de004c517684397c0b90e76`  
		Last Modified: Fri, 31 Jan 2025 01:33:36 GMT  
		Size: 122.0 MB (121978371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ec2be59cd417822f2376c1db4c2c4131e7ffc35b935890dc18c6a69dd76e83`  
		Last Modified: Fri, 31 Jan 2025 01:33:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea2bc3fcd9284cdc46d7b62693c6bc21ebdc4961b386581131ff762d77a1607`  
		Last Modified: Fri, 31 Jan 2025 01:33:34 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:999a4332a43bd70f5dd17523958ed51a0890fadbbfc5929334d929dc63d73dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84c79c2505929241fe353c601e380aabf7e1700c9a13c4b3b4faa561e9da042`

```dockerfile
```

-	Layers:
	-	`sha256:27b96dd59e709c2946824e5c76c2626b157bd8d28934b6480bf7663e829d77a5`  
		Last Modified: Fri, 31 Jan 2025 01:33:34 GMT  
		Size: 3.7 MB (3673527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5cf4cf2248b56b5971aee7e78338294b2faab2045580298458a5ccc3f9bce38`  
		Last Modified: Fri, 31 Jan 2025 01:33:33 GMT  
		Size: 21.7 KB (21715 bytes)  
		MIME: application/vnd.in-toto+json
