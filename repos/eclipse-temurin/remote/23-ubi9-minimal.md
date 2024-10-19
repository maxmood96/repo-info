## `eclipse-temurin:23-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:f34b98a7a71a5c8cdfe36241abe1b8bda84f23a16e9fc88b905283f8cd78ab27
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
$ docker pull eclipse-temurin@sha256:45d5233b0d620e34536124e659d24539ecb5f88ef2230737e4205b1a38c65255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235373199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dba5a5bd91cdc9a49c152f55d968a4fae94227b2628a66fc849e35f0810a4dc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 19:12:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 19:12:13 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 19:12:13 GMT
ENV container oci
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 19:12:13 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f266998e95c628e5d1212e5fc818ff539865ef4ca545a0b46c6b912ad922938`  
		Last Modified: Sat, 19 Oct 2024 00:56:30 GMT  
		Size: 31.0 MB (30993820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d884199ddadde5cd8fd204bfbcba7a009ab74858cb982c7b3ac42dec65e091`  
		Last Modified: Sat, 19 Oct 2024 00:56:32 GMT  
		Size: 165.3 MB (165275434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04598e066bd93f82c8beec7df5168af85a6bcead92799b522eec1cbdefd28958`  
		Last Modified: Sat, 19 Oct 2024 00:56:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2928aca26fb8ca9d75ccc4c345ad66a1b414de51f29e7217296baba02cbc7c`  
		Last Modified: Sat, 19 Oct 2024 00:56:29 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3cf7c83fe7113e572a42991d025cd071269e9d99e85d508769e67ac62c40c057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6318be6a5e26f574a14c831b4190cd36df269de1bd51703277719a849fa29bfb`

```dockerfile
```

-	Layers:
	-	`sha256:6fcaae7732e7da5a1e385d932565562b0ec04cf6ae73360659d6c22a6821236f`  
		Last Modified: Sat, 19 Oct 2024 00:56:29 GMT  
		Size: 2.6 MB (2568436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3036cfbf0ca43800a11fa3d4319e6af17db5758d76bdd9c465669b5bcfba87bc`  
		Last Modified: Sat, 19 Oct 2024 00:56:29 GMT  
		Size: 19.7 KB (19695 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:046ef1d2b78817f7c2fcf9ee302a4f18ed1ae0b2336a6279c7baa6d6154521e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231541535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefe214808c52cb2e9fa3eeac4fce5f84f9f0f7c07eb8e81ec791c6d850cec68`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 19:12:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 19:12:13 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 19:12:13 GMT
ENV container oci
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 19:12:13 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17c1f3d1069c55923e15f6f6cddcc3378a0c14bb4e83ccb03296abdbf5ea9f5`  
		Last Modified: Sat, 19 Oct 2024 01:13:02 GMT  
		Size: 30.9 MB (30942147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b28f38cda516b928c8eeeed3e04d7f50d8abe70d0fff65549087b56a9da5`  
		Last Modified: Sat, 19 Oct 2024 01:20:41 GMT  
		Size: 163.3 MB (163261728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f8406cb5219a656ee1e82cf414ade6e8b087d7636624648629b2f7719d3150`  
		Last Modified: Sat, 19 Oct 2024 01:20:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc640ff94af39db6b731602eb252163912bbcd210993ebd67326ac199557b1e5`  
		Last Modified: Sat, 19 Oct 2024 01:20:37 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7fd49d74c92920a9db19039a5cd46a859d49452af5d80555adfc04a037088a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0377c5178d52b9f639cde2b0721fa176110f249fae1ab1ddbd71a892d08c517`

```dockerfile
```

-	Layers:
	-	`sha256:5a6130c445ac3a34c0e56e8c66dda3ceb9b20e9fef06b0807783fe1c69e18ded`  
		Last Modified: Sat, 19 Oct 2024 01:20:37 GMT  
		Size: 2.6 MB (2567089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9851178cf31186115060772cd8710ba26524e9a8d885f3d0c3da960eac1255d`  
		Last Modified: Sat, 19 Oct 2024 01:20:37 GMT  
		Size: 19.8 KB (19811 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e67cb98ec7de25635e3052136c22d6036e223a62ec323373e94cbe3f4e7a27b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243948550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3220ee97337c6566775b597a48af748d1cb2207d94a3f899177825152da2b5cf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:768947e71543f3d306ccb7844a46e1e32556950241f32410fa419d064856cb19 in / 
# Wed, 18 Sep 2024 19:12:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 19:12:13 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 19:12:13 GMT
ENV container oci
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:b67c0e7a04afadb6a5c642b16810b67dc1863b7bbfbb7821e18e5a4992e865c2 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:b10d88ff3ef2f9f197c2e406b732bc1a4de03c114efc0060dabb5d8a0ace9e3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 19:12:13 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e31ac149cb4a1eda22cb8c0e4ae005a8c53c5e2e4fd29c118b346755b642aeb9`  
		Last Modified: Mon, 23 Sep 2024 18:10:35 GMT  
		Size: 43.6 MB (43591438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1350de893f773003630b1ca55b7319237d47f1b98f468ae0e4f88d86d464f8`  
		Last Modified: Sat, 19 Oct 2024 01:00:14 GMT  
		Size: 35.2 MB (35196719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefacde0d1922373323e50f0ba97d2ce20e732f353d927e07cbf7d3022585ccc`  
		Last Modified: Sat, 19 Oct 2024 01:09:49 GMT  
		Size: 165.2 MB (165158146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4543a3031e4cec64a53c02ec7a304d594dc42ec71793232ed5b2b09b12510da6`  
		Last Modified: Sat, 19 Oct 2024 01:09:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e8d1c3411094af2489c00e71468cb4c0be91b7d28cdff65d2e7b2514ae3a0e`  
		Last Modified: Sat, 19 Oct 2024 01:09:44 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:43534693d05d46d00f56e2f9520eb54d872e5d678640c78b5f529508651f7534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce64859c866332c863f9e7c8158e1fc8bd3c66fb29c7bef8022f6b3f25a2ce0`

```dockerfile
```

-	Layers:
	-	`sha256:026d359a700ab481f72e701a741b72f584032ea9a3556838abe0a4c3c16ea7e6`  
		Last Modified: Sat, 19 Oct 2024 01:09:45 GMT  
		Size: 2.6 MB (2567108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3becd7f2a3cdbb9e561055d98ae25c36eb6ea05c110f2dc0153b9deedd1c28`  
		Last Modified: Sat, 19 Oct 2024 01:09:44 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3c0307d64a6be9a5c9e3ee5b907e8552b9c26bb012971d79ece69838b263b2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222258528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fed03caaace054eb43bf46907ecfced47668361755c8d3a0fe234972d9631dd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:21b7ed3b2258da5b5d030b86d62b0787dcd37b89f90dcc66430117025bb05f28 in / 
# Wed, 18 Sep 2024 19:12:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 19:12:13 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 19:12:13 GMT
ENV container oci
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:ce3abbd79cb8c99cd1c0e2f5562e76837cd37c2684866f11810f889122c06843 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:ac24882cff4e990075d0c05821308e37e323ed349a4be0a2192cde67bcc09b3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 19:12:13 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 19:12:13 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d38740decc88f04976b3123db64216586005286cafbf52d64706fa02375bde9`  
		Last Modified: Mon, 23 Sep 2024 18:10:42 GMT  
		Size: 37.4 MB (37364487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594a80d63c227d0475753011666179dfe483fedbe4fcd6ae725ef9f11ab589ad`  
		Last Modified: Sat, 19 Oct 2024 01:00:25 GMT  
		Size: 30.5 MB (30521152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b2faa7c8174c5930067ec801e418cc8d06320fcf581cf32f647757afa278b`  
		Last Modified: Sat, 19 Oct 2024 01:06:42 GMT  
		Size: 154.4 MB (154370646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0561bb2af78da8d81171492360402e2dcada506ceb0a1fbc338686fb43ba777e`  
		Last Modified: Sat, 19 Oct 2024 01:06:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c542c80c9ca5f5085c30bf0b5fa93ca15a143fae4578f87efcbcc1854ed2a84`  
		Last Modified: Sat, 19 Oct 2024 01:06:40 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cb5df32ab4610b9434972bb70ed9dde759d72a8bf2d456abc7c6fb7d4ece321c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2576066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf18c02ee6e7958e7fd126c7daf7fcbbb07854f911447d2a833f6fbfde5dc91`

```dockerfile
```

-	Layers:
	-	`sha256:9c2915ca6e2c485b619ac4426cac9fedd68a2331c24015251622086171c21b77`  
		Last Modified: Sat, 19 Oct 2024 01:06:40 GMT  
		Size: 2.6 MB (2556372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a34c9997c24e86730dc7f1c443fb849ddd73d6d57c77f71452575e8cee44ec`  
		Last Modified: Sat, 19 Oct 2024 01:06:40 GMT  
		Size: 19.7 KB (19694 bytes)  
		MIME: application/vnd.in-toto+json
