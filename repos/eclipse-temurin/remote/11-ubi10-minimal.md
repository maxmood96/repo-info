## `eclipse-temurin:11-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:9f1e58e90c10424833f109c250d5e5750a8b694361bc3b97d3c6561b482b03c1
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

### `eclipse-temurin:11-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:171aa72a9fd621fd566b45840497c3fd5c749100b447397b04c9371152b917c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.4 MB (213382077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255b2b3463470ca784b4c49684972f62b91d8cd82dbcda940f1dd0450a91553`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 29 Jan 2026 09:02:30 GMT
ENV container oci
# Thu, 29 Jan 2026 09:02:30 GMT
COPY dir:fd123199d2aa564f8f0592613ffa5ec1622b80265ee6073edb50ec5ee7520e92 in /      
# Thu, 29 Jan 2026 09:02:30 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 29 Jan 2026 09:02:30 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 09:02:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 29 Jan 2026 09:02:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 29 Jan 2026 09:02:31 GMT
COPY file:449edb9408a04a948eac072a18a188bbaa8b86d792fecd68574017d6afe608e1 in /usr/share/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:02:31 GMT
COPY file:449edb9408a04a948eac072a18a188bbaa8b86d792fecd68574017d6afe608e1 in /root/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:02:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="24312baa53bef28621c8f52f140c638d591e1d71" "org.opencontainers.image.revision"="24312baa53bef28621c8f52f140c638d591e1d71" "build-date"="2026-01-29T09:01:57Z" "org.opencontainers.image.created"="2026-01-29T09:01:57Z" "release"="1769677092"org.opencontainers.image.revision=24312baa53bef28621c8f52f140c638d591e1d71,org.opencontainers.image.created=2026-01-29T09:01:57Z
# Thu, 29 Jan 2026 19:04:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:04:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:04:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:04:53 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 29 Jan 2026 19:04:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:04:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:04:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:438bf0ef7bf7d9e54cbea537827e1b65c9de6ea0f4486cbdeaa845a0a9e70190`  
		Last Modified: Thu, 29 Jan 2026 10:51:29 GMT  
		Size: 34.6 MB (34577419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d84b1517a8cd5efb61d3c14fa334d164f47cde267cfde78764f14ba05e898`  
		Last Modified: Thu, 29 Jan 2026 19:05:16 GMT  
		Size: 37.4 MB (37376999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9303c14ed3cdc7e0efbbb121e97627c05096c36ad63011fb9fef2784f1806c`  
		Last Modified: Thu, 29 Jan 2026 19:05:18 GMT  
		Size: 141.4 MB (141425238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0e68f4de343f6ea8b1f73827d17f162f084015fd799589ed6bc4dff84ea0e2`  
		Last Modified: Thu, 29 Jan 2026 19:05:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073541b0413201f946aeb8abbe98309c2e16e4b96802ee54a602d51becc24799`  
		Last Modified: Thu, 29 Jan 2026 19:05:15 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3795bd6577bcecb0bac556b0e2866d6bf8df3a5153511ef9eddc5cda65f76201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616f67e5bc39b4dcbb2e25a16d9a3241abb5fb03dae23790aca162277f3da98f`

```dockerfile
```

-	Layers:
	-	`sha256:e8d5b4f007075f550af98000f46432f2b3f374f95e2bc778686014958d756ff4`  
		Last Modified: Thu, 29 Jan 2026 19:05:15 GMT  
		Size: 3.8 MB (3807969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67361bdf4a0679d3be123a4d66afaa423a3a435a030de5f0c13577bd77fff1a6`  
		Last Modified: Thu, 29 Jan 2026 19:05:15 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:fb1cf239c3d70640c09e921a4f25dac58dc0be08a5a155cec49f0a604afc3323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208215406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cd4d57580279925de63c6700137bb3f9fabe2514460c39f11b5ce9f8f79312`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:56:41 GMT
ENV container oci
# Wed, 04 Feb 2026 04:56:42 GMT
COPY dir:67028d43c1066b84b1209232f64f1a4cc4b9dbbfba57178bd9cbb9c32d30e9e7 in /      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:56:42 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:6daaa71ff7be172f731620b1d0190bb9c2177930f1dd64e2221f2ce09f100fc6 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:6daaa71ff7be172f731620b1d0190bb9c2177930f1dd64e2221f2ce09f100fc6 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:56:43 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:56:21Z" "org.opencontainers.image.created"="2026-02-04T04:56:21Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:56:21Z
# Thu, 05 Feb 2026 00:07:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:41 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 05 Feb 2026 00:07:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:07:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:07:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:07:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:07:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e7aaef72f9aac8066ddd0c18bcd7c76fcc63212a965d38f195e0959c666aa7ce`  
		Last Modified: Wed, 04 Feb 2026 06:11:32 GMT  
		Size: 32.7 MB (32661097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1b05ddd3568f8d445cf323298b543ab3e2f566036c07ac94a811a49309f7f4`  
		Last Modified: Thu, 05 Feb 2026 00:08:10 GMT  
		Size: 37.4 MB (37361610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a1e9a155caa97dc55a2b17c59718b26610a7c2963cb577eafe62946dd56021`  
		Last Modified: Thu, 05 Feb 2026 00:08:18 GMT  
		Size: 138.2 MB (138190280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07948583d9d5e2e138cc415062a7b2e7811c473b706e045bb98a4764148539bb`  
		Last Modified: Thu, 05 Feb 2026 00:08:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66a7f64de2e6a9d634836fff196247823f6d5bcaaebe8523b5e7b1b503226f`  
		Last Modified: Thu, 05 Feb 2026 00:08:06 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ffd46356ffdee347f0829542e3192d65229643b2277285f0027f750c45c522ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c089ba6a520bdac2f7e91b7cb53461ccfe407d17c9176fc211f48f011a69e03`

```dockerfile
```

-	Layers:
	-	`sha256:e0ab2010c836190fd8c7fb961e0716ce608d5a76028f17745bdbdf6fb802ff23`  
		Last Modified: Thu, 05 Feb 2026 00:08:06 GMT  
		Size: 3.8 MB (3808069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12db552049b400a75b0e28b27836efbed8bc7b72c0ea6a57733684fc141e27f5`  
		Last Modified: Thu, 05 Feb 2026 00:08:06 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:2dcac24666c6455ca2a3245832c40ac75298497ea33ed73ed98b7f28049b8f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206394991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0336ebb2181b10e65dc152e9d033041ffa10652e0843e30288b35762e9f1c95c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 29 Jan 2026 09:43:39 GMT
ENV container oci
# Thu, 29 Jan 2026 09:43:40 GMT
COPY dir:9f05c03fd98385ca667703832b015e247b162c40641da4bfafae12b451fb75f8 in /      
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 29 Jan 2026 09:43:40 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:53726944e41cc90bd970a2878ac432c863bd39ac879813f59a75e5ef00cb4ae2 in /usr/share/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:53726944e41cc90bd970a2878ac432c863bd39ac879813f59a75e5ef00cb4ae2 in /root/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:43:40 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="24312baa53bef28621c8f52f140c638d591e1d71" "org.opencontainers.image.revision"="24312baa53bef28621c8f52f140c638d591e1d71" "build-date"="2026-01-29T09:43:27Z" "org.opencontainers.image.created"="2026-01-29T09:43:27Z" "release"="1769677092"org.opencontainers.image.revision=24312baa53bef28621c8f52f140c638d591e1d71,org.opencontainers.image.created=2026-01-29T09:43:27Z
# Thu, 29 Jan 2026 19:28:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:28:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:28:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:28:25 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 29 Jan 2026 19:30:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:30:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:30:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:30:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:30:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8e4c90395db70569d5d34c1b72c9a955f03527f82047f5ff481b9771e26f723`  
		Last Modified: Thu, 29 Jan 2026 12:10:46 GMT  
		Size: 38.7 MB (38665536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a847da3c495b4477c38c514638ee54d51d2e0860a704b7879a5c13e9d797ec8d`  
		Last Modified: Thu, 29 Jan 2026 19:29:12 GMT  
		Size: 39.1 MB (39142692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73cf5eb6702f257c5600a7176b2665b7dfd1556f4a4b541a1a35f7b737d98e3`  
		Last Modified: Thu, 29 Jan 2026 19:30:42 GMT  
		Size: 128.6 MB (128584340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5e63a73c6c8c29b3625a205205f7c3f50f71c0a15f5fb1d5fab5e7ebc7793a`  
		Last Modified: Thu, 29 Jan 2026 19:30:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb0a6ba79547b87420320c6c36db5834994028cf9e13f4a0e2ea7c5fc05e6a`  
		Last Modified: Thu, 29 Jan 2026 19:30:39 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:eab635480cde638afdac74e3d209db337aaa2daf9cec05866bc9503742f23c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9dce7136626e0182d215820b09d568082ca5d38dac2257e25d19d877a7f3f0`

```dockerfile
```

-	Layers:
	-	`sha256:c70b73a075ce437032c1783459ffa94619ca03910d75d4d38a70aee565875db1`  
		Last Modified: Thu, 29 Jan 2026 19:30:39 GMT  
		Size: 3.8 MB (3794186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392442295fab52e733b69dae76f40def9585d7298ff2c888cab05a7777e13cd0`  
		Last Modified: Thu, 29 Jan 2026 19:30:38 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3f21e9481614a4d3c8f3c7a3750caee02ac6631e38a34c86552627d3a1039295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194300385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627c8907f3738e87d306ca831ff2f21b1e4f417399e920efe7877f7a476cfc84`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 05:11:29 GMT
ENV container oci
# Wed, 04 Feb 2026 05:11:30 GMT
COPY dir:9d4ac575a92f53870377be4b68b1588c9bc427ee283102569774f3d9158a16f9 in /      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 05:11:30 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:bd2f18d5b9d97db31e1a3f98a0670c0f15ee13ca2c036700589166ed0ad3221a in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:bd2f18d5b9d97db31e1a3f98a0670c0f15ee13ca2c036700589166ed0ad3221a in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 05:11:30 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T05:09:09Z" "org.opencontainers.image.created"="2026-02-04T05:09:09Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T05:09:09Z
# Thu, 05 Feb 2026 00:07:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:02 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 05 Feb 2026 00:07:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:07:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:07:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:07:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:07:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c5e6ba1d838b1d4e103e0457068eaff01f71c8436e4442eaa2f5c701ccbe1c6`  
		Last Modified: Wed, 04 Feb 2026 06:11:43 GMT  
		Size: 34.4 MB (34399700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19d1328bf4040759158c3f4a9ecc47912b1ffb1b173eb92519cea4b9d9c9de`  
		Last Modified: Thu, 05 Feb 2026 00:07:35 GMT  
		Size: 37.8 MB (37794412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e32fb7ff74e2e020fa9182cc249a15c290ae0b7473fedfffda048b2794a732`  
		Last Modified: Thu, 05 Feb 2026 00:07:36 GMT  
		Size: 122.1 MB (122103852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252bba06f778a0a7725e72dda0846d6af4306d135f5f6331e8e21190680b9d74`  
		Last Modified: Thu, 05 Feb 2026 00:07:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd66d2e2a6b7bd1597367a367cd0c37fc15e28b839c0d11137ad003a2fff3490`  
		Last Modified: Thu, 05 Feb 2026 00:07:34 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:296e30fc22a3fd079f4ac568ce721a38bbb1146d804a9aa92e13118fcc19cacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23030ee8675eed24c62c79731f82164399c75184e4c8cf3798dc643c9c08253`

```dockerfile
```

-	Layers:
	-	`sha256:573c2b48bf1ed2e56a639dd62af0296c4f898e932974ee869ff1d6e62e7fc555`  
		Last Modified: Thu, 05 Feb 2026 00:07:33 GMT  
		Size: 3.8 MB (3793619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f9632b9b6626933606d3979daa80430b549032baa16a749efbf7d19e5fd125d`  
		Last Modified: Thu, 05 Feb 2026 00:07:33 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
