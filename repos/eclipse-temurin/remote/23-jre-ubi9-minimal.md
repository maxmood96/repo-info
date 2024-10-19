## `eclipse-temurin:23-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:e2f43c444fa001dda34e9dd6795bff2feb9220cd1c8a5faa69fc85ccd4a55bbc
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
$ docker pull eclipse-temurin@sha256:6718a1b1b284c06f66b07627048628b243c27dd1a32a7faea18cab0c2520333d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123043855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e57b0dd6c6a19cef135938a5f639bbc2b15b62ec04435da3ba9e21600504ab7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534bce430ae107739cb91fe3d9a339c0833b1ace78318f36d7bae8d35f28c32a`  
		Last Modified: Sat, 19 Oct 2024 00:59:34 GMT  
		Size: 31.0 MB (30993988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3106acf71a0c3f591b65b0fb1b90f52f2084bb3a15c511a5edffb887825b840`  
		Last Modified: Sat, 19 Oct 2024 00:59:34 GMT  
		Size: 52.9 MB (52945925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dc864f0752933b67cc2ed4ec4f7481572b25adec8b475bca659e4af6bb5ef4`  
		Last Modified: Sat, 19 Oct 2024 00:59:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f035dd81d2e79c777cb0d0562e3bac3724f57ea1daae61c0c78faf102af674c`  
		Last Modified: Sat, 19 Oct 2024 00:59:34 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ebeb946055d03e9ccc6b9f8af40efc4958eab3387ecb30c8f16cc5ce5c960088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d26bd35aa566d84974eacde9ca0026d728ad4ddcbda0e5b3bcb464a06dc9c6f`

```dockerfile
```

-	Layers:
	-	`sha256:05f909314a862a768871f8a4aec0dcb499d52eb5f28d914a4574adf4e07bdfa6`  
		Last Modified: Sat, 19 Oct 2024 00:59:34 GMT  
		Size: 2.5 MB (2482563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c4ea3f8a775666ef01e35593f0655bedd3b88bdbeeaa7428d4bf4c6f62fe83`  
		Last Modified: Sat, 19 Oct 2024 00:59:34 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ccacb389f6ca1a34383be126e0ba0e6854acb4a030783c019798cef2fe2b8fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120248860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea351bc5de5d5740b1c754d99bf251839644ead5163329356a8df3b5af697ea`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
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
	-	`sha256:23e990c03db2931bcc18b8aec3bb5b3e52973a47d4ae9b47f401a264f5b61274`  
		Last Modified: Sat, 19 Oct 2024 01:21:56 GMT  
		Size: 52.0 MB (51969057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e9b617a0d1c34a948db119cba33884a89261f9d50ed6ba092de40ee54124bd`  
		Last Modified: Sat, 19 Oct 2024 01:21:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01afe6585b6d02ae3bb5aa7b5092f48ee21d65c9168354a6a97ca84236cbeba9`  
		Last Modified: Sat, 19 Oct 2024 01:21:53 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e4f438054263b2ecfaf0a903b164ee9345269d3d3bf83f8f23195b523aa917ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2282cf595ae41a2117b4ac31b4aef3ceadfa6351e8e91bf219ce54e92a349bd`

```dockerfile
```

-	Layers:
	-	`sha256:e8a5f1fb480116d5b08a7f541855e50c7ecd3a78ecd46136e4d362565ac219a6`  
		Last Modified: Sat, 19 Oct 2024 01:21:54 GMT  
		Size: 2.5 MB (2481204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f611274308bda15e6ab4bd9569ccec483215e8ecf871479158528222a3cad10f`  
		Last Modified: Sat, 19 Oct 2024 01:21:53 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e30dadd2ff8de0acbe1188099d9d7f4c5a7357c5267d69040ebb7a267742eb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131609729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5b0f13e3afcbdbe9f9e9285275ee28e8cf80c456ba06d70f782a18feab0346`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
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
	-	`sha256:edfc234d6ed04f798717b4c3cd08d4e9b93fe6d0ba7e0596aaaa5c5da3159197`  
		Last Modified: Sat, 19 Oct 2024 01:10:41 GMT  
		Size: 52.8 MB (52819334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6294f9438b8cf07d793e509775eb99a28ef8f6c64202b13764185475c939d8a`  
		Last Modified: Sat, 19 Oct 2024 01:10:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4fef421ca26152727bbd1fbfece187740d4725bb564e7b2df216ab53f0b5d6`  
		Last Modified: Sat, 19 Oct 2024 01:10:39 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6dd7853f50357fb9260d00f62f5db77d8aa8d78677d3846ee63fc0f7f7ef9728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1892a19610c521a677bd160565cb9c21b1075a1897bb76586b87fbc705b971d6`

```dockerfile
```

-	Layers:
	-	`sha256:ff2328e0d7c09a64f885f35ebb39a0a192a478f8f81875ff684524277629d733`  
		Last Modified: Sat, 19 Oct 2024 01:10:39 GMT  
		Size: 2.5 MB (2483139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a077a3c02ed5c881423c455a6ccf09e21d305a6a211da7a99e51eb67f85da8f`  
		Last Modified: Sat, 19 Oct 2024 01:10:39 GMT  
		Size: 18.8 KB (18824 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:d95677cc510818807a985478cad62447bd0d4fcc2d4d0e128e657591b7b292be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117328759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b2f40cd8a9cae35ebb79e35bd198272e5db278dc6bb3c28263ab0259d42fae`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
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
	-	`sha256:4de6e392a013c3788f5bebbce65bb6e9c66cde856b916bb9d013f43a5996098a`  
		Last Modified: Sat, 19 Oct 2024 01:07:26 GMT  
		Size: 49.4 MB (49440877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a304f54a5c547bc77d9c0e642e44d533d7a09c508c31078b66541b60b98d26`  
		Last Modified: Sat, 19 Oct 2024 01:07:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2e7a039f84f457589636beb026beb5939417abcb55a86a517cf962e584bf04`  
		Last Modified: Sat, 19 Oct 2024 01:07:25 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:030245aa787241e745ff794eb0db89e3445fbb5d1041a225cb83cc4c41e4d1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2493688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8656432f1078002d70e3c14b373e327c5b26b1e9c880dd990029cf95bef1b80`

```dockerfile
```

-	Layers:
	-	`sha256:6bf7d97b4541f6fabca5a291292784164c7045a9d480227daaa48acec909b93b`  
		Last Modified: Sat, 19 Oct 2024 01:07:25 GMT  
		Size: 2.5 MB (2474894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63608b4e986ae8092634ac060c80173f8765f9acc4e82a803ae6e86d1314f96b`  
		Last Modified: Sat, 19 Oct 2024 01:07:25 GMT  
		Size: 18.8 KB (18794 bytes)  
		MIME: application/vnd.in-toto+json
