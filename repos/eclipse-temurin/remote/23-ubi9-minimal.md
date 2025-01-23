## `eclipse-temurin:23-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:d4ae7b256d0a142c21fa531434f5314e2c64c317da3529c5644583483ba4e554
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

### `eclipse-temurin:23-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:da3e8c26a1bff5e6615a43142ab0bd61cc8cd25f3e1fc4277e9b4f0dba294af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241729064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c543a452fa57d5ef903b04560833686dfbfed064beffba0f8ef0d756297fe585`
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
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
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
	-	`sha256:7638a8e113320fb1a8fe53323e4946ca517f3f1c21711e8f68e0a9aef989b648`  
		Last Modified: Wed, 22 Jan 2025 18:29:28 GMT  
		Size: 37.0 MB (36989312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d741353d9baa0532630724c15eb6175d7a689ae1a4292b103eddfa8da69eb2bb`  
		Last Modified: Wed, 22 Jan 2025 18:29:30 GMT  
		Size: 165.3 MB (165304507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a834db5f0dd4b5fcfdfbfcf17cef566418f3ea47d65428807669b1585267dda8`  
		Last Modified: Wed, 22 Jan 2025 18:29:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcaa2ac83ee528c780d4bfa9d26718566f6063eef11f7ae7fe76ad2faebec94`  
		Last Modified: Wed, 22 Jan 2025 18:29:27 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:79bc626a949b8b421b2d2803ff6cc5db1885000cdcc0d6947e6aab745add8b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3693515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e89b8dad5bb08129db725e83ade145fe423a1ce746185d084134b41797eb43`

```dockerfile
```

-	Layers:
	-	`sha256:8e77b4bdef340177b0da2c8570394f5c9aa39d328d14064c18cb414d8ed8fb2b`  
		Last Modified: Wed, 22 Jan 2025 18:29:27 GMT  
		Size: 3.7 MB (3671801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f73781832f8554924f61b4dc25d7aa6ec18fee34e2296f6f92e0a5bb4b9e0d`  
		Last Modified: Wed, 22 Jan 2025 18:29:27 GMT  
		Size: 21.7 KB (21714 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9e60a56f2169bff9d3566be121ca4305a0b1ce1223051d7316b7dad427144a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cab7684c9366fc283f74a8943a52cce7e48266aa6759717fa0984be24a8afb`
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
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
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
	-	`sha256:1d63414ea28d2f723fd2f9e80c3dd680450b052dabf18a756616d3e64f636607`  
		Last Modified: Wed, 22 Jan 2025 21:15:57 GMT  
		Size: 163.3 MB (163290123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8e3b110ae3d05945347b102dd78631be5b256b319a09dc4349e46e177fede6`  
		Last Modified: Wed, 22 Jan 2025 21:15:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871b57d15fc1271518ec7864cc350e70d198cdc3fff9109140a9f71602994a05`  
		Last Modified: Wed, 22 Jan 2025 21:15:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:61021393ede973cf8e079a7164deb7aaf9b2965d605a422eb25faf2c8720df14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f910cc394aa8edf52fdca299b9489ede7a687e1bfb5cac8cadeedfd13d36ee`

```dockerfile
```

-	Layers:
	-	`sha256:4bf872f5e817eac7096d703668e4fbd02d27b247abcf7c0bb9e3fec7d224bea9`  
		Last Modified: Wed, 22 Jan 2025 21:15:53 GMT  
		Size: 3.7 MB (3670371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b943d03ff8a055a79d3486645f7d4a86b812c0b4d4c778744a46ad19ebc2cac0`  
		Last Modified: Wed, 22 Jan 2025 21:15:52 GMT  
		Size: 21.8 KB (21831 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f3802c9895d0b6ad02f446969831d0ca9c722586cd3f3ac3934c020b999405ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248461411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ed58fe3c732ab4ba762420614e093292a69799768533ab0f3bf01030df2b6b`
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
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
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
	-	`sha256:885cd4a2198e23751aec51fc046432b6f8dbf8c42877684f55d821802d5717e8`  
		Last Modified: Wed, 22 Jan 2025 18:59:44 GMT  
		Size: 165.2 MB (165187796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dfac01af5a21658cad0e235429540f883ed6f738d7e55b11ee2e9da7dbd420`  
		Last Modified: Wed, 22 Jan 2025 18:59:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e963b70dcc7d2bc13498114adba63eed87f4930057f5c166653fb4b799b91a`  
		Last Modified: Wed, 22 Jan 2025 18:59:40 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a3af3ca9d1bfc3a1073839d60244b1e050ac0bc71d199417379bc7648dcb5932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692f293c8b3c87b42db926ed2eae682b327df8434df183ba7b6a4bb29f5874cb`

```dockerfile
```

-	Layers:
	-	`sha256:d1756d3dbe79e2fede6a6ffca0855031491bdb06b6936a06b4b7882af5e100ac`  
		Last Modified: Wed, 22 Jan 2025 18:59:40 GMT  
		Size: 3.7 MB (3669105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6bd555b929b70a5a2ff5e75e261cebf20cf508214120db85f7799cf06d0d07`  
		Last Modified: Wed, 22 Jan 2025 18:59:39 GMT  
		Size: 21.8 KB (21751 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:4ce8ac0f0049f7023f4168b4efb987e015e726bf700ef1311fc860b6aa9ee3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228954915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9548579dce48cdcb23c205a6545c768325f084ac6732012b8b427e36129076`
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
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
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
	-	`sha256:95dfd0b1e9e894253f6fe8cfcfba7f6013e2e08a28cc0ffcc14687af9268d07e`  
		Last Modified: Wed, 22 Jan 2025 22:12:57 GMT  
		Size: 154.4 MB (154411909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249f86b709759a13d271727220a18d80eef7bf479da3f9e451c3d39ab10ff1e2`  
		Last Modified: Wed, 22 Jan 2025 22:12:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec379d6ab603934eefa1a3c818a0ed2c4e4d7b014c94f6c931e9e4ed8863030`  
		Last Modified: Wed, 22 Jan 2025 22:12:55 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8edd391047e89d320472aef651cb63e5071f69471d3e62119927ad4817cd60cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5affab70cff404f7fede934dcbdf3419cb776f658e5705c31b1372d090efb8c`

```dockerfile
```

-	Layers:
	-	`sha256:4b4e2e87a8ad8469ba8e0550df789fb526e2797081a8aa083bb1955f3713a753`  
		Last Modified: Wed, 22 Jan 2025 22:12:54 GMT  
		Size: 3.7 MB (3658405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a7928bfcf41c0fc65b0d2449c659a24533ecf28fab9a8cd5094f0ee1430512`  
		Last Modified: Wed, 22 Jan 2025 22:12:54 GMT  
		Size: 21.7 KB (21715 bytes)  
		MIME: application/vnd.in-toto+json
