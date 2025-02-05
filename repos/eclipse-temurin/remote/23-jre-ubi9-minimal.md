## `eclipse-temurin:23-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:ce57e08f91c7bb108bd7dc9218b1dc7d7a1379221cf6a3e6f1763e8068246640
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

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b045feb93345c521bf88297a19c4cb840e863e06e0acbca886f5631e55b17f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129329815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d631ea0f212260b66549c106ed5c345e988ee46912427afababc90497cde1694`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:791945992d1a1a0e69cb46f548168dd778c0a5b28228ca7d157145f53fdb49cd in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-04T04:38:14" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
# Thu, 30 Jan 2025 14:32:57 GMT
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64le)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:24436b52f270faaf1cd45508746ed85af4420ecadbf33becda289f2e4221eb18`  
		Last Modified: Tue, 04 Feb 2025 06:12:46 GMT  
		Size: 39.4 MB (39370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7773c651ce2558c22521f6ea1bb2e11b3a7e0f291de522fb1183c6ab4e62c1a6`  
		Last Modified: Tue, 04 Feb 2025 06:12:45 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026efda676723ae83b64f05100f369ebdc42f2df55e374224b41b674f0949c0`  
		Last Modified: Tue, 04 Feb 2025 20:33:05 GMT  
		Size: 37.0 MB (36988071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb018189465e0954d4f5f00b1a71a57abe1ee770791184476b56ec7c97f84300`  
		Last Modified: Tue, 04 Feb 2025 20:33:06 GMT  
		Size: 53.0 MB (52967935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4b6b52055f92cab4690ef83ac40f465bbe0553c9d245c687b2dfb987a7eb4d`  
		Last Modified: Tue, 04 Feb 2025 20:33:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2356edc3fb5334763e6a52682a4bda10fe549c165c323d7cbac70bd6b984ec61`  
		Last Modified: Tue, 04 Feb 2025 20:33:05 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9693e442b3fa36cb587f26d9a3835dbe670c1a3999cd94c24fff8cc5444911cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a586e7a9cc79d42d82ac886fffc9608885b4ff4d33874dccb4a71b10ad1ffb9a`

```dockerfile
```

-	Layers:
	-	`sha256:05f2997385e7db1e009c11e7add0617507053877872eb82c1c8c8ad4e3971748`  
		Last Modified: Tue, 04 Feb 2025 20:33:05 GMT  
		Size: 3.6 MB (3586073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d56bb1b336812275fadd28e7585e074b79b17f4fce8e8c223c19953f85be06d`  
		Last Modified: Tue, 04 Feb 2025 20:33:05 GMT  
		Size: 20.7 KB (20732 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:108f373e30ec3723bafd1e7f11b93457a21c3d38f9551a7bfc34003a4064cba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127057854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94998845e85bf238752f4e0712c6dfc861176dd57e5b85e2c9942d9102d48f1a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:9a473b4852f6cbe9a0f08b40d1fff87f485e10a0b3973b8009cae74075e5e063 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-04T04:40:56" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
# Thu, 30 Jan 2025 14:32:57 GMT
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64le)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:93168a48887270ffcd74fa1e7b5a85a6420b35b7dca5a5971f063fb8a0d3264a`  
		Last Modified: Tue, 04 Feb 2025 06:12:53 GMT  
		Size: 37.6 MB (37592781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b362866ca09649c77058b63f51549ffa71c5ffce326fe4b42995cfb1180db`  
		Last Modified: Tue, 04 Feb 2025 06:12:52 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84479dead7bf933b66919d3f2ec6e0c436e237743bb05b2641923502bc6498ad`  
		Last Modified: Wed, 05 Feb 2025 01:56:02 GMT  
		Size: 37.4 MB (37442468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725873be52865fd369f533519f5206b3b89cbbe10ee99470dae0f08df0b53f79`  
		Last Modified: Wed, 05 Feb 2025 02:00:59 GMT  
		Size: 52.0 MB (52019725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b226b3f35bda4349234b8b091fbf7ad9e5428f6812c5ffeca326f51eba21120`  
		Last Modified: Wed, 05 Feb 2025 02:00:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199afa90bae9b824e73aab15674a54fb990a5dd8de11b8c44c65230df892e8e1`  
		Last Modified: Wed, 05 Feb 2025 02:00:58 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e43b4e0e69dc3e932c25f820375c3648c14c98171ea5af5ef4f414c8e930c1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2c82a7e6078fee295651d3653b101ed0af9ca6e152e499b89474233d9d3d62`

```dockerfile
```

-	Layers:
	-	`sha256:d7f406433cf3168e95709628a6c1af0d00cedb80f83b3ce9e240499fc6b4237e`  
		Last Modified: Wed, 05 Feb 2025 02:00:58 GMT  
		Size: 3.6 MB (3584631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4fae517c56a73367c4c0265d1308726349506cf56339c1bbd5a277446e28bd`  
		Last Modified: Wed, 05 Feb 2025 02:00:57 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e66798dbd207bf998d8990d3d83546da7d16ff0a36172b74ddff437852ab82f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136140392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9f017d543999169db500ead4dcadf68d21bd10a645db734a8416d7cefd5960`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:86eaaeeda22f0fc1610df3530c5b1f3ed71bded65fc4f1a6f230c64b6243fd6f in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-04T04:45:48" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
# Thu, 30 Jan 2025 14:32:57 GMT
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64le)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ab1f86d0f34fa967c24e957a9589d5e97ac11fbc48f1c47f2ad66357588ea649`  
		Last Modified: Tue, 04 Feb 2025 06:13:08 GMT  
		Size: 43.8 MB (43812384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a26502eee0ac1b566e8c1915dcb2d87d299688b9b9004feafb89ec7b29c48e`  
		Last Modified: Tue, 04 Feb 2025 06:13:06 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347e995a3ea744fbc6cc7a931bed349b6719e0856e76ac20c2e4b79b93870d5a`  
		Last Modified: Tue, 04 Feb 2025 22:22:34 GMT  
		Size: 39.5 MB (39477501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cd53b7f34ffb031317d49f4076bf7ad02cd7209b5164b9a485f60bae5232bf`  
		Last Modified: Tue, 04 Feb 2025 22:31:30 GMT  
		Size: 52.8 MB (52847630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d28a66982cc4fe44013a4fd4e819d81b076c7722fa7a81744a991db5c8800`  
		Last Modified: Tue, 04 Feb 2025 22:31:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c495b024143e1335f9f12123db7d2f23ce044018190efd5e34a7cc919d90e3`  
		Last Modified: Tue, 04 Feb 2025 22:31:28 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:73e569fb7eb11a904249d381b1af68e13f77e3829fac98246e865edbd2c04ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cb567284a01bb4bc965d6e0294fda58db919e80d8b8b005d55b83735f71899`

```dockerfile
```

-	Layers:
	-	`sha256:ee54bf4e17512d5266700343986283d8455a38a2349dc4f39c7d66bdeebe5b25`  
		Last Modified: Tue, 04 Feb 2025 22:31:29 GMT  
		Size: 3.6 MB (3585278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cbbb7f799c0fe5abb98874ffb0a5f0e1aa37d0bb65cc57f0bb231193941e98`  
		Last Modified: Tue, 04 Feb 2025 22:31:28 GMT  
		Size: 20.8 KB (20762 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:da7cf039aa972aa7c18145cd8fefad857044444a22cc19a8ac7b72a28518dcb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123974247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804a1e483b58950337c389ee926fe57aa136f97ea35cc8d19e2686c1ed0acfb8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:e4f2c18684ff5ef7306326b55f2c892a9155159af76ab7e5cd185fec25280bc1 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-04T04:44:01" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
# Thu, 30 Jan 2025 14:32:57 GMT
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64le)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f2c60604373bca3b723153547f9e3eb1b61b4624a6533a0e44a4a24b3a6a5fd9`  
		Last Modified: Tue, 04 Feb 2025 06:12:59 GMT  
		Size: 37.5 MB (37509933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffad1e63add1f545943d65ae14bc90751c2d7d5a9bf5feb6dde9cdf16d6faa0e`  
		Last Modified: Tue, 04 Feb 2025 06:12:58 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d8dde926e1cd7b699bd4757bc6b3441a0004e029140a4dfd9157b6d0cd6670`  
		Last Modified: Tue, 04 Feb 2025 22:36:20 GMT  
		Size: 37.0 MB (37005223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30970d99fc196289cde0aa5770d26de9365334291fb1ff7ad97463b4cc520abf`  
		Last Modified: Tue, 04 Feb 2025 22:44:21 GMT  
		Size: 49.5 MB (49456214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9387a2ed2d38140868f17e4e715b713f498ca4377fee3450aec5d68f8ed5e14e`  
		Last Modified: Tue, 04 Feb 2025 22:44:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284df3887186f83863a520773a9b3d57427cb15eae0d00610f30c5e86eb10070`  
		Last Modified: Tue, 04 Feb 2025 22:44:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5dd10a9a1337b59c5d055065037ca30b8159399dec84a958235e539d24f4f26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d7776dd4297f265650aae6655a9ae9370b01c4eb052101829bb77c12162ba`

```dockerfile
```

-	Layers:
	-	`sha256:ab338163032d1646b663f200794ec6738f718b4686ecff6aa371f76f65befbb9`  
		Last Modified: Tue, 04 Feb 2025 22:44:20 GMT  
		Size: 3.6 MB (3577065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352b870a62ee0b690e51c1ad710a3469ea97269f8258ee2dcbf4d577e5242a07`  
		Last Modified: Tue, 04 Feb 2025 22:44:20 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json
