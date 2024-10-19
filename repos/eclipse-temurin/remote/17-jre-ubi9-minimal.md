## `eclipse-temurin:17-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:6f739b142e72a22e9bd6363245a29225ea110eb2a255bab3c3b52deb8cd8bca7
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

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:dc3e7b5c399b4517c254b92e9387f321f1c090a504c5f2637be3c4add78723ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117379431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0065ecb903648ac725a194eec5a3e5a207833fa43ca31c467e5d7574a2e2b4d8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Thu, 22 Aug 2024 07:58:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 07:58:33 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 07:58:33 GMT
ENV container oci
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 07:58:33 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64le)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        x86_64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dd2c6b3db81d01c69b1d330073fda56f3a312654617895df4de8626ae8d1a6`  
		Last Modified: Sat, 19 Oct 2024 00:55:12 GMT  
		Size: 31.0 MB (30994044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbf5843ea24c75ba915900f187f5a12b9e40c58c0187f5008bc6b0f66feddab`  
		Last Modified: Sat, 19 Oct 2024 00:55:13 GMT  
		Size: 47.3 MB (47281444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d873804c59fdc238c7bd80cfec11ee83d3dfccb5790a596bdf3a6468beb2f`  
		Last Modified: Sat, 19 Oct 2024 00:55:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc658ab430c1f5c41972dfe25df3c33eee02886e5eb2297191d32e278debf14`  
		Last Modified: Sat, 19 Oct 2024 00:55:11 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8e0cacb9e2884296cef91dda25c405d580a23b1eac9b51165cf57d0603dd84ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2497085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56226e92bdd2bdaac4ffdb8b4e0e7bd27ee1476a53a66e71079b70f92a3c0d9`

```dockerfile
```

-	Layers:
	-	`sha256:085fa41ef296751cef52d6ebb008c86737ae416a866e8355052d3ec6d25370ce`  
		Last Modified: Sat, 19 Oct 2024 00:55:12 GMT  
		Size: 2.5 MB (2478195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f2c8a7126cde285a1569408fdc495ea4dc102881fb1549150bd6ebce266706`  
		Last Modified: Sat, 19 Oct 2024 00:55:11 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:cc787d53f98bcf7954266ff38351f212fbe3d9a396ba6197d81da2c16fe6ac11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115024180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24196eab37785c7764199ca4996044f4f42a3b20f69f8cbb3d529c1705454ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 07:58:33 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 07:58:33 GMT
ENV container oci
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 07:58:33 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64le)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        x86_64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:800fc6400ad11cdb9824ede83a8cc810e44e0a7e18f71054d9bb2cc0c1ca9a6b`  
		Last Modified: Sat, 19 Oct 2024 01:16:19 GMT  
		Size: 46.7 MB (46744376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05b1134b7789c65593a9695be7829350849b1e8c147a6cef8e96f9c1f10aa1`  
		Last Modified: Sat, 19 Oct 2024 01:16:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128ac4f2a2021d4996eb9de1ba4cdec06269278689c5d88e8a5d2cc484d8009e`  
		Last Modified: Sat, 19 Oct 2024 01:16:18 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:50266de5145a3a1d5d7390c66d6bb582d6533d730496016230ae2aa62d0fca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7e7a00f46070021ab3a22eee42976c93a2cb0c7625abeab20c6fcc7f798668`

```dockerfile
```

-	Layers:
	-	`sha256:bbf0a4d93e1d7e2cb0d31fef024b4ffd3a6c45b2f22cc0fb2c7549c3b1ca0749`  
		Last Modified: Sat, 19 Oct 2024 01:16:18 GMT  
		Size: 2.5 MB (2477458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd65f26f3a40e344764b1c70c524af163c76b270d06e43d4d46d405f5594eafe`  
		Last Modified: Sat, 19 Oct 2024 01:16:17 GMT  
		Size: 19.0 KB (18994 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0bb9229ab693b7d21844df28e87a30a46f62bb3665223485603460954806fad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125916105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04029b69819d57cce139771598aa5688382a732db14acda171f7f35921bffca2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:768947e71543f3d306ccb7844a46e1e32556950241f32410fa419d064856cb19 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 07:58:33 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 07:58:33 GMT
ENV container oci
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b67c0e7a04afadb6a5c642b16810b67dc1863b7bbfbb7821e18e5a4992e865c2 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b10d88ff3ef2f9f197c2e406b732bc1a4de03c114efc0060dabb5d8a0ace9e3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 07:58:33 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64le)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        x86_64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:172e4793170bce33422b11a1f9701f3feba0f97f235e743b748bb410fba5faec`  
		Last Modified: Sat, 19 Oct 2024 01:06:42 GMT  
		Size: 47.1 MB (47125706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1257b6abc73bb9062bc5fdb4300e2fb690880cce86056564cf32e3baa1732d8`  
		Last Modified: Sat, 19 Oct 2024 01:06:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7159cbe728dcfaa36bdf65300842c1a26087613c3f3f6d5075836f125eaa57c9`  
		Last Modified: Sat, 19 Oct 2024 01:06:40 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:786564869a1a74a97bcbe257ffcdc1be1da87dd891f541e356dcb706a2765b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df77b352f909952e93ddb97df08146e4f18dbd40f4d1cc416acd21df0c291f78`

```dockerfile
```

-	Layers:
	-	`sha256:56826d111fbf6f443f8e765fb2b48a8bdb0bf4ce397f31ac9a939a170c10ad7e`  
		Last Modified: Sat, 19 Oct 2024 01:06:40 GMT  
		Size: 2.5 MB (2479393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a658a154207806429a3af35c84e528a7651e82aeec9b299f5f2b90ace7d1f0ba`  
		Last Modified: Sat, 19 Oct 2024 01:06:40 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c3317f2f3ca792b57d2c66b672ed1cbda6fa3f8858e430e674d70b7a16bd78fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111742325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadba849645ed8131ae42ec432638ce46a8860866a1610e4e7d18ccea35a1795`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:21b7ed3b2258da5b5d030b86d62b0787dcd37b89f90dcc66430117025bb05f28 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 07:58:33 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 07:58:33 GMT
ENV container oci
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ce3abbd79cb8c99cd1c0e2f5562e76837cd37c2684866f11810f889122c06843 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ac24882cff4e990075d0c05821308e37e323ed349a4be0a2192cde67bcc09b3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 07:58:33 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 07:58:33 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64le)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        x86_64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:64e302017dec132157c5c05f4b17d87ea38b987f0d2509541f752ef761c7f5d4`  
		Last Modified: Sat, 19 Oct 2024 01:03:27 GMT  
		Size: 43.9 MB (43854443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce212452e1d5f1996379f8ec661a00083b791e39468b00862fa5b4f411950a9`  
		Last Modified: Sat, 19 Oct 2024 01:03:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06950939c5834528803d1ebb4d350d8801d144137e3988470e126fb84b431aa5`  
		Last Modified: Sat, 19 Oct 2024 01:03:26 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:50e456538c1fa5520f6f593049e149bd583202f63a55ec0afcc76475d6ebb5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2490037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f9cd652f40a903bda6df6e4035ed5c5d80a221281db6a86635c2b7ba61a334`

```dockerfile
```

-	Layers:
	-	`sha256:31183ca31c239097b5153505078ba76b9cc7a85f0b7ec47efaab8a371905f16f`  
		Last Modified: Sat, 19 Oct 2024 01:03:26 GMT  
		Size: 2.5 MB (2471148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11119f4005de220deb18780535f4a5a2f0d47a3d940278e1fd80a1fd515b67e6`  
		Last Modified: Sat, 19 Oct 2024 01:03:25 GMT  
		Size: 18.9 KB (18889 bytes)  
		MIME: application/vnd.in-toto+json
