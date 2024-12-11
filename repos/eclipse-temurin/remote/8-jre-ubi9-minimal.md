## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:5671bb66b5a17fca8c90c915c28996eaa6aa5f32829e45859179362a76238b1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7bffa2572b78d2d7f826b72df8e7d296ed326f1d60bf4a4e9042c367bb65c433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118292268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1706e8e761fada2c2c950a94b750556560097381981f406fe019d6e6de9bdaee`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b45099af11143c90baeee19296763e905644154c1ed853eb5968678d4d61054`  
		Last Modified: Wed, 11 Dec 2024 20:29:46 GMT  
		Size: 37.0 MB (36992647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dde342b4d13a32c1c683bc2922cb608f6c6f13a3a831213512bacf8fc08d34b`  
		Last Modified: Wed, 11 Dec 2024 20:29:46 GMT  
		Size: 41.9 MB (41877907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160383e0ffce36ed5fa15d4e4eb8878b80071af131023399120d20fca1ac73e6`  
		Last Modified: Wed, 11 Dec 2024 20:29:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210320d1eab34e9f8674ecaf179d18d8ecbe73da2b34436a1c2d6551f626809d`  
		Last Modified: Wed, 11 Dec 2024 20:29:44 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4c318a00063a9e291ae9bf2d45e925e5c8a8d6c4dd5ce1eb890685cda40e9d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3639492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfff5bfc5a63f15deaab5b559363cd05c535b961df13edbbec9a7b2dbbbd4cc`

```dockerfile
```

-	Layers:
	-	`sha256:59469e7450f49e870be924bc16f62eec5a375233024d223eeb7ad43bad1c10e4`  
		Last Modified: Wed, 11 Dec 2024 20:29:45 GMT  
		Size: 3.6 MB (3620288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508b7c448cc3bf4cc20c72f52f07046dd320c1f5b798e5044459ab48153239ad`  
		Last Modified: Wed, 11 Dec 2024 20:29:44 GMT  
		Size: 19.2 KB (19204 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7e034fc4e271ecbdc3cfd7e3f70b12948128da77a7b5fecd0d07742fc1a24443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115961545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a1c5199cc7b8f43385eee2a83e6dbb74553688c6b3874388f93f0facc4bb71`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e16a7178cd631e8e68738f34a2f20d3ba24d9ff892dd572f951fc36b2476268`  
		Last Modified: Wed, 11 Dec 2024 20:38:41 GMT  
		Size: 37.5 MB (37451094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624d51329239dad650a50042339ff4849aad43aa00934dff5861c09483c8621f`  
		Last Modified: Wed, 11 Dec 2024 20:39:08 GMT  
		Size: 40.9 MB (40860507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c955babf041fd057dc82cf11b49dc88c670ef1db44ff0f4d96db5cf8a607cda2`  
		Last Modified: Wed, 11 Dec 2024 20:39:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8185b19383972f9f25cac9a6fcd66df3fd745a6d8d2ac63e3c715291f89d543`  
		Last Modified: Wed, 11 Dec 2024 20:39:07 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:85f67fffc7fc2c95747683d296f1f3f23986346e050f0d18f21ec6cacb2e57b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3639550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02495ca4d8bb064d22b506fdfbebfcf2a0eca5bf0190ea42e39d14995ed0b9cf`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2faa7ea4022289475af2c23a3e95c7818af9d47a1b83c425a90a7876feefa`  
		Last Modified: Wed, 11 Dec 2024 20:39:07 GMT  
		Size: 3.6 MB (3620242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d4811aa42a445240ee314876a6ed107161ca35236c3c7d3f7fb3eb306976f1`  
		Last Modified: Wed, 11 Dec 2024 20:39:07 GMT  
		Size: 19.3 KB (19308 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:c68c84f97dab93c8e94aab639711f4218581f906840e64342f173a1defa0cc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124526947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5588db8a7f20cc4d2c1c781df3175dadb2c19fbd4e91429a397f7a6319c76a9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:8f21bb638bfc9999eb0c06c365b4f63918e550b9f8a3df9bb94983276e9b11a8 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:28:12" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7f109adddadf658534777a91b226ce1bc9f7dcc45f9c30eea9c0e426aadaa062`  
		Last Modified: Tue, 10 Dec 2024 00:14:54 GMT  
		Size: 43.8 MB (43801042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d525a4c647a13d8db1417c57a1dc81822cc7796bf044edd48aa9d99ca6ee58`  
		Last Modified: Wed, 11 Dec 2024 20:32:31 GMT  
		Size: 39.5 MB (39476600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f25c2dbe1268f1c30bb0ce71916eca87b301b3f3d86040eb866a88d050a1d68`  
		Last Modified: Wed, 11 Dec 2024 20:33:22 GMT  
		Size: 41.2 MB (41246885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f8804159b65e06f83da3cb72764c40911b3313906b6a5f3ec263da187b8eed`  
		Last Modified: Wed, 11 Dec 2024 20:33:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a63b81129c60c65bd8222c01bfc99cb19a4c7fc3646a0f49710570b82b2e42`  
		Last Modified: Wed, 11 Dec 2024 20:33:18 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e3b24bdeb5c9f4f28718228838b492b499057cb53a52e7b2988279a85cef3f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9326d16e8a13032a3fe3e2180470a739e89f157ceb6665abaeaf395400d9125`

```dockerfile
```

-	Layers:
	-	`sha256:3cc252da08cfe98d0aa5815504f2e44c9506bffc426b359113dd414891462ad9`  
		Last Modified: Wed, 11 Dec 2024 20:33:19 GMT  
		Size: 3.6 MB (3620907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54da48603428d5ab1c56b7adc70f7aa6772d17ee4cae3d9ddc716325caeb046d`  
		Last Modified: Wed, 11 Dec 2024 20:33:18 GMT  
		Size: 19.2 KB (19234 bytes)  
		MIME: application/vnd.in-toto+json
