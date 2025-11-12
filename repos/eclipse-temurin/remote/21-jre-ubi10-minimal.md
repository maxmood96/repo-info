## `eclipse-temurin:21-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:199a16edf216de5b89c381912ee70e30f380df72899f4123e6bf4929d88eb70d
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

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d480a708c622e8a12966f6eb51d2705af0e8f29173c2625c2af473025e7fd185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144811142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6d74499d9b10698f0bfdf2b6b5a5c62a1c99f3cb58abd09a75a29c1a31bdff`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 17:11:09 GMT
ENV container oci
# Mon, 03 Nov 2025 17:11:10 GMT
COPY dir:b2070c3a584696dfa50295995b98f1ca6f69ef03e4ee4a779757baf0b56a1546 in /      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 17:11:10 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:11 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T17:10:18Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:38:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:38:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:38:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:38:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:38:44 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 12 Nov 2025 18:38:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 18:38:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 18:38:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 18:38:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e2fb7c31c3da29493a9042fb2aac284034d054c3aa5fe92e1f234b9e077ede47`  
		Last Modified: Wed, 12 Nov 2025 00:12:41 GMT  
		Size: 34.2 MB (34167037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99851141f0ed581d692487d708c3684f3f1e8661f038abeb1b16b22bd0f273a1`  
		Last Modified: Wed, 12 Nov 2025 18:39:18 GMT  
		Size: 57.7 MB (57665394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d4994e6cb1c494576824bae51e0f1e46377dfc5db06f9ae8e6332645f26d1a`  
		Last Modified: Wed, 12 Nov 2025 18:39:19 GMT  
		Size: 53.0 MB (52976294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461258ecf01d71290cf029554b038f0d93f40b70d211cfd7cc7104e5c72f130`  
		Last Modified: Wed, 12 Nov 2025 18:39:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad3d9fafc51138c38d6fd9e6989a78564125179e3db33f4d5d2f49c75b29c6c`  
		Last Modified: Wed, 12 Nov 2025 18:39:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d73328805a996d5838b0cde920cef2dd57eda9be2b065c482527342bd2c63be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1030d9146bc8b995d9e93a6d0a19f813911f579c4b9d3b70545cde861a7ff1`

```dockerfile
```

-	Layers:
	-	`sha256:11f7710dd689a5241bdb02695296ec5b546cc6fdeb42919f0cc4873bae1befe7`  
		Last Modified: Wed, 12 Nov 2025 19:14:55 GMT  
		Size: 5.6 MB (5598917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182450d1d5717886ff0f351ecd41a8996b8fe333aadc2af1edd08f61373b7a91`  
		Last Modified: Wed, 12 Nov 2025 19:14:56 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:bb2d97da0d18eeb9587e2f843932469d1864a1f8819f7d67f77ef767cc65962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141792398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ec088a1babf932047bfa7d4a3b00ff11844955600008373ab65772fbee2be6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 17:14:06 GMT
ENV container oci
# Mon, 03 Nov 2025 17:14:07 GMT
COPY dir:c8db51b55d4ac263e724340de097ab5a5aa8fea3d84a7bc887161a3f2c5d43d6 in /      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 17:14:07 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:fb36c295d366f4dba8ba95e1629c37ca6425e3e98ba006db98d86ebcf2c79b44 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:fb36c295d366f4dba8ba95e1629c37ca6425e3e98ba006db98d86ebcf2c79b44 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:14:08 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T17:13:46Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 19:39:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 19:39:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 19:39:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 19:39:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 19:39:46 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 12 Nov 2025 19:40:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 19:40:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 19:40:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 19:40:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f1037a79a8a82585aa3e6b5df2e6c0a42e2f3def0513fef76cfd1daba7331879`  
		Last Modified: Wed, 12 Nov 2025 00:12:43 GMT  
		Size: 32.2 MB (32192138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f039385de436536a4878fc5323e0650e6e10bd76a940bcf77df2c0e85b3718`  
		Last Modified: Wed, 12 Nov 2025 21:00:35 GMT  
		Size: 57.5 MB (57456658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83038432f98e750eeaaf23650aba361b5222b2bb5d384f047f9a3778af4ca65c`  
		Last Modified: Wed, 12 Nov 2025 19:41:20 GMT  
		Size: 52.1 MB (52141187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31123e0db0720674a61facb9059d43fcba16a73d8d50c8899e44aad91cf1af34`  
		Last Modified: Wed, 12 Nov 2025 19:41:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f31c8ff9ce810ca9418a82111e414dd7e3dacfea31b560397da338aab732955`  
		Last Modified: Wed, 12 Nov 2025 19:41:17 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b02359886257fe033c5a3dc1019a6b76610290e26769856eacd14199851c1ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5381bbe34101446ad1db5d1ff78755ebb72bcebb0c193de2b41f9cbe3f49d03f`

```dockerfile
```

-	Layers:
	-	`sha256:67b14c891bf237d10f922ddfb8dad9f24fe7997b19baf1806486877ce7b46205`  
		Last Modified: Wed, 12 Nov 2025 22:14:30 GMT  
		Size: 5.6 MB (5598395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70f4505c804f0898cf740a647593979d687b5e01310d63b23cef32613f01b47`  
		Last Modified: Wed, 12 Nov 2025 22:14:31 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e1882cf0c635884ac8a00745d88e557e738343063125503543986ed6b4064a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150894420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5aeefe28a4cab7d0fc7ebe6375f76410333f45a6469840826df03b6f9210ed`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 18:21:17 GMT
ENV container oci
# Mon, 03 Nov 2025 18:21:19 GMT
COPY dir:bddbfbd27697aed0d6ba6e3639d53eb2bcbf54a469bc264141734564ee0873d3 in /      
# Mon, 03 Nov 2025 18:21:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 18:21:19 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 18:21:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 18:21:21 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 18:21:21 GMT
COPY file:db0b3bfc9b0c5f121f2453bb59e26e6e1b4ab566a800db9e34c541da8076e42d in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 18:21:22 GMT
COPY file:db0b3bfc9b0c5f121f2453bb59e26e6e1b4ab566a800db9e34c541da8076e42d in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 18:21:23 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T18:20:23Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:51:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:51:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:51:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:51:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:51:18 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 12 Nov 2025 18:59:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 18:59:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 18:59:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 18:59:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f0606a13920710459cad07c2d91ffb3bc0d8c2d18eb333131c2e90dc0ae025c2`  
		Last Modified: Wed, 12 Nov 2025 00:12:42 GMT  
		Size: 38.2 MB (38231260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c0fa2afff4fce2da3348f13f3ff118dfa655106daf72e83b8d728ab5a3304`  
		Last Modified: Wed, 12 Nov 2025 18:52:31 GMT  
		Size: 59.7 MB (59682969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a73bda0e2aacb6d125f9f7892c6c290bb0e55ab0d8d8578fa258e945eccd87`  
		Last Modified: Wed, 12 Nov 2025 19:00:40 GMT  
		Size: 53.0 MB (52977774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbddf556e8c4044a9537eab934ddc2a9a8f518d5e893a1b520dc2304ab96336`  
		Last Modified: Wed, 12 Nov 2025 19:00:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ee04286f3ce64d1523dab14320a00d0e907964eb3ce4c219a3d98c2cb0ea1`  
		Last Modified: Wed, 12 Nov 2025 19:00:38 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3abc7e9de833021ee593c7baac15e3c029dc6c6b17b88a2992ef6fd14371cb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2dc45ba788f3ba009ba86dcc71d8cedbc67d9ecf1b6b9689b5a599ba8da87f`

```dockerfile
```

-	Layers:
	-	`sha256:d42a4325eba948becdd1f4eaf14b667676feaf7eddebb862e50f4a6625083639`  
		Last Modified: Wed, 12 Nov 2025 19:15:07 GMT  
		Size: 5.6 MB (5587982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f0d139a1842d3bc70a12496fba34129f45798feb82650235cbb508662ee0bd`  
		Last Modified: Wed, 12 Nov 2025 19:15:08 GMT  
		Size: 20.4 KB (20384 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:11c47b2390344d84cc42b004f70d28c62d918b2b403e0e10879981886c549e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114970987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3537b5f64930a07a90040937012477dcf533b37a564631230231b04ee23b2bc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 11 Nov 2025 09:53:26 GMT
ENV container oci
# Tue, 11 Nov 2025 09:53:26 GMT
COPY dir:9f1f5449cb9454b7c05550f990009868329830ff5f598e41882e09b2985f76ce in /      
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 11 Nov 2025 09:53:26 GMT
CMD ["/bin/bash"]
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 11 Nov 2025 09:53:27 GMT
COPY file:d3b5fde18206481b740a53df7391a42dcce042cfdd4edd5afeeb9637f6b9111a in /usr/share/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:53:27 GMT
COPY file:d3b5fde18206481b740a53df7391a42dcce042cfdd4edd5afeeb9637f6b9111a in /root/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:53:27 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "org.opencontainers.image.revision"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "build-date"="2025-11-11T09:51:11Z" "release"="1762851739"org.opencontainers.image.revision=0a583d401ee29f56bb3786d762c71b4349cd93d9
# Wed, 12 Nov 2025 00:25:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:25:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:25:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:25:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:25:26 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 12 Nov 2025 00:40:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 00:40:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:40:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:40:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1276be387a6a7c4ba51d350a6bfba6a1c72fe42d07414791e01dad4ca06bc732`  
		Last Modified: Tue, 11 Nov 2025 12:10:44 GMT  
		Size: 33.8 MB (33797474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94e9c54bbb60d78e3a1b2c270640fe5278b731547a8566cca26aacb7fbf74d5`  
		Last Modified: Wed, 12 Nov 2025 00:26:59 GMT  
		Size: 31.7 MB (31655122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f62d84af792516fae08c0fe401a1f3007133cbe097a085f2a9999c5dbc45448`  
		Last Modified: Wed, 12 Nov 2025 00:41:33 GMT  
		Size: 49.5 MB (49515975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7047f7d53f7b85ae1a4b81aeb20cea5766d8454cdf625776ec83e14101e3321c`  
		Last Modified: Wed, 12 Nov 2025 00:41:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277b7aad3a32cc14f4153fcda59401785f92e90e189bf31489edd7b7ddcc54c2`  
		Last Modified: Wed, 12 Nov 2025 00:41:24 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:163807077fd568fc27428530d3ab874cab7defd6ed5c14f9c9a46c208271ca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f6896cf41df7ba8c674ff00aea0a57a0d48f8591da41b52010a286921e52b0`

```dockerfile
```

-	Layers:
	-	`sha256:17d0e394625b05ac0c8167ecdf9a996bce7fd44b41e72f2cb4cd6dc2d73d319a`  
		Last Modified: Wed, 12 Nov 2025 01:16:25 GMT  
		Size: 3.0 MB (2981435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874ac088520f9d9804881670b79b91f8960455af0f81537e3d1d3cfe43f9c306`  
		Last Modified: Wed, 12 Nov 2025 01:16:26 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json
