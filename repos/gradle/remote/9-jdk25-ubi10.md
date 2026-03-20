## `gradle:9-jdk25-ubi10`

```console
$ docker pull gradle@sha256:77779345f38e4c6222123fb23c025efef65e59074c3067bb15d5422a7625f812
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

### `gradle:9-jdk25-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:74bf7df1bb50a19ae0bb60a749e420443ee4c6232c28567eb53a9f1464ed4425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340877342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6c46b2e48cfd8e1bc0996c35afdfb20d282414a538a7620c68249fe4ce2498`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:53:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:53:01 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:53:01 GMT
ENV container oci
# Thu, 19 Mar 2026 04:53:01 GMT
COPY dir:af440ed069b945cf125ef868e769f70d1b1e33071b111d96c1e9a1ffc5f76e4e in /      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:53:01 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:6585c86973269b2041af40b485e0e6f045b49959f72c04fee4a05795e2e5a97c in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:53:02 GMT
COPY file:6585c86973269b2041af40b485e0e6f045b49959f72c04fee4a05795e2e5a97c in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:53:02 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:52:47Z" "org.opencontainers.image.created"="2026-03-19T04:52:47Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:52:47Z
# Fri, 20 Mar 2026 00:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:17:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:17:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:17:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:17:24 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 20 Mar 2026 00:17:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:17:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:17:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:17:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:17:55 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 01:10:25 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 01:10:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 01:10:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 01:10:25 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 01:10:25 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 01:10:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 01:10:29 GMT
ENV GRADLE_VERSION=9.4.0
# Fri, 20 Mar 2026 01:10:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Fri, 20 Mar 2026 01:10:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 01:10:32 GMT
USER gradle
# Fri, 20 Mar 2026 01:10:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 01:10:33 GMT
USER root
```

-	Layers:
	-	`sha256:f862e22eed3c55bcf45baceaa7dd39dbd424275e0f2d3130583784c94e488dfd`  
		Last Modified: Thu, 19 Mar 2026 06:14:45 GMT  
		Size: 34.6 MB (34610902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c04fcb3cefc56b5fa03c76ff01b2b9df689b3b272c4e364903f16ce68fd9d37`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 37.4 MB (37446929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6713951577462f6197446adfaf2cd004c214b7017c3b6c522a5d611576475dab`  
		Last Modified: Fri, 20 Mar 2026 00:18:14 GMT  
		Size: 92.3 MB (92257965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4413150d64d2a1b5c73615df91697080d17af836e682b17ca733c463bd988`  
		Last Modified: Fri, 20 Mar 2026 00:18:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fa8336613eb9e021af5b3f282cc46cdc62253859733e27b29ee43192693f10`  
		Last Modified: Fri, 20 Mar 2026 00:18:11 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f41b5ddc31a3c83dccc0e9a2a1ca9e50aeece5cff0b017e0bde91e6415388b`  
		Last Modified: Fri, 20 Mar 2026 01:10:52 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6566554a5eaa8c0d09ddaf3023924233eee754ebe96246c2276461b4b66a8c`  
		Last Modified: Fri, 20 Mar 2026 01:10:53 GMT  
		Size: 38.8 MB (38758733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c52c6f2c6d8af0596b9856aa92c98d7654af3c50a75ad1466aec1bd3de027d`  
		Last Modified: Fri, 20 Mar 2026 01:10:56 GMT  
		Size: 137.8 MB (137773166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e9ba848adb9007d67495487e0da17d788933ee904db9a170d1e94772dfbff7`  
		Last Modified: Fri, 20 Mar 2026 01:10:52 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:f00043a5d221fec4b62aadfc9a99b3af05acb7ffab56eee143b5acb70b648ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef1c05e97c80bc2a97b470e882f2818485e1b6c98bd4f5ff56e2bd7c9e8cf22`

```dockerfile
```

-	Layers:
	-	`sha256:dc6713e648fd315ec85c034a021cb37e0e92404227f705840f8724513612d7ea`  
		Last Modified: Fri, 20 Mar 2026 01:10:52 GMT  
		Size: 7.0 MB (6994902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd13f794b0cdec1140ab3b61a723f03ed39785730f1a57060732b543ce9923e`  
		Last Modified: Fri, 20 Mar 2026 01:10:51 GMT  
		Size: 25.0 KB (25013 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:188c946e1fdc7f47403c82fa9bc006df8e5b875bcafd364bed6ad2f3af456816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337425181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ca9e206bd601f630161ac273655c6a33c1aabb635ee5238f4350bb080e782a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:55:27 GMT
ENV container oci
# Thu, 19 Mar 2026 04:55:27 GMT
COPY dir:ddf23ac9073f2f0aebc549dd652158e51758019b3f147b69bcf85b8c51fd9394 in /      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:55:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:3038f4da402f5d3deadca7034502c693a744bf96305b10c79908db4a59bf74a2 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:3038f4da402f5d3deadca7034502c693a744bf96305b10c79908db4a59bf74a2 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:55:28 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:55:11Z" "org.opencontainers.image.created"="2026-03-19T04:55:11Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:55:11Z
# Fri, 20 Mar 2026 00:15:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:15:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:15:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:15:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:15:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 20 Mar 2026 00:15:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:15:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:15:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:15:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:15:11 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 01:10:49 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 01:10:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 01:10:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 01:10:49 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 01:10:49 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 01:10:54 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 01:10:54 GMT
ENV GRADLE_VERSION=9.4.0
# Fri, 20 Mar 2026 01:10:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Fri, 20 Mar 2026 01:10:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 01:10:57 GMT
USER gradle
# Fri, 20 Mar 2026 01:10:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 01:10:58 GMT
USER root
```

-	Layers:
	-	`sha256:32559d11b9ee98b34627afd92e663006f6191d5024358c48c175361f14b3bf84`  
		Last Modified: Thu, 19 Mar 2026 06:26:47 GMT  
		Size: 32.7 MB (32683055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10fbcf144660556c5a7344ab4608530851325a049c81d215ba3760221cee3b5`  
		Last Modified: Fri, 20 Mar 2026 00:15:29 GMT  
		Size: 37.4 MB (37383254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc214319c2abef0b7f026b91370bb31f92544c7b5eced36b6f62b3f6342b43d5`  
		Last Modified: Fri, 20 Mar 2026 00:15:30 GMT  
		Size: 91.3 MB (91297850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055672969b006d395f2c74ef0f6ecbb42054df25f6834ffe53c47d1032349f16`  
		Last Modified: Fri, 20 Mar 2026 00:15:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238f923118d46ff12e781385c6a25fe99cf4b0f593a80c25180d6f34983d3fa5`  
		Last Modified: Fri, 20 Mar 2026 00:15:28 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba54e0313bfd9fb53d80fd1638609d69a11ccb0376e43da7c9e59bfd13d3433`  
		Last Modified: Fri, 20 Mar 2026 01:11:17 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0a46d818f0170a0bf5538aa2d0d277d0b9e1f67f646f10c939a1242fab4e0f`  
		Last Modified: Fri, 20 Mar 2026 01:11:18 GMT  
		Size: 38.3 MB (38254491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a37715482db0ac76c5acae68a651973a1ea1dcbff85b96c35479bff338d955`  
		Last Modified: Fri, 20 Mar 2026 01:11:20 GMT  
		Size: 137.8 MB (137773160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3b517baebacc09d9fa0eff8930efdc69c0b96beebf853b0c5fb27ab49b2bef`  
		Last Modified: Fri, 20 Mar 2026 01:11:16 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:8d418c9415a525d659bee938d07a9494a7cc590f637e24c393f4b6607904d75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7018413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b196689f33dafb44a19ee0cb799177e76f460f2a8e7284c70169ca0bcc0451`

```dockerfile
```

-	Layers:
	-	`sha256:018f961ad4ac6449ac0a469c6b039178ffd97306f36edbb42e1e3b7616d3056d`  
		Last Modified: Fri, 20 Mar 2026 01:11:17 GMT  
		Size: 7.0 MB (6993179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9df4b3c682b863f3497b4a0c7ca24117ef023a953c325cd93c5198d636ff093`  
		Last Modified: Fri, 20 Mar 2026 01:11:16 GMT  
		Size: 25.2 KB (25234 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:773a146b952547a04eab9355d203eb1a8376b33516fe068e81193fd877ff2325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.8 MB (347847533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc65f462c4c324c384e82b80244d1fae43afe889a4de06dc1a64b9c04d33649f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:54:26 GMT
ENV container oci
# Thu, 19 Mar 2026 04:54:27 GMT
COPY dir:02874e9a4cbd11d21ae5a0b0d5ceabca448e8e4b7d87ed83fe20e3fe3891053a in /      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:54:27 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:cd93def3bf43c5dabe55bff87f8d330823b7a378238d571cd76fa53ae8fb0d3c in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:cd93def3bf43c5dabe55bff87f8d330823b7a378238d571cd76fa53ae8fb0d3c in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:54:28 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:54:15Z" "org.opencontainers.image.created"="2026-03-19T04:54:15Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:54:15Z
# Fri, 20 Mar 2026 00:02:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:02:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:02:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:02:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:02:04 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 20 Mar 2026 00:10:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:10:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:10:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:10:06 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 01:09:21 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 01:09:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 01:09:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 01:09:21 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 01:09:22 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 01:09:54 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 01:09:54 GMT
ENV GRADLE_VERSION=9.4.0
# Fri, 20 Mar 2026 01:09:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Fri, 20 Mar 2026 01:10:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 01:10:02 GMT
USER gradle
# Fri, 20 Mar 2026 01:10:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 01:10:04 GMT
USER root
```

-	Layers:
	-	`sha256:d4c7683a582dd524d9a529f07d62fb8d8a6768403c45eb8da73d739aaacbbd8e`  
		Last Modified: Thu, 19 Mar 2026 06:27:21 GMT  
		Size: 38.7 MB (38730914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cb46297f5b33cc4db0990c621afa3066c8a88767766b1d83c47221837e903b`  
		Last Modified: Fri, 20 Mar 2026 00:02:45 GMT  
		Size: 39.2 MB (39201421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328398164b8913ecb2b16547ea61e11d8ce6c0d80567a7051156e941bb03194`  
		Last Modified: Fri, 20 Mar 2026 00:10:45 GMT  
		Size: 91.6 MB (91634888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f551f87074551bd32528a8adc16932c978553c1bd961ddd304af422cd6c1589e`  
		Last Modified: Fri, 20 Mar 2026 00:10:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d523cf40311a087d77797706582123633e3dfe4be351705ecff49d4ea8894c`  
		Last Modified: Fri, 20 Mar 2026 00:10:42 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd7d5a0ab43a3de4a06ebd41f81f216677feb567af2e249daa13cb7875c826`  
		Last Modified: Fri, 20 Mar 2026 01:10:48 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c3cdb48c170882ce60522ed97c0e0c2c24c5b0f4cc2ba2c9a0952879f84950`  
		Last Modified: Fri, 20 Mar 2026 01:10:50 GMT  
		Size: 40.5 MB (40502736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bd5182014c7ca82f9f24c52a9c98863fcbce0ab568de0ff74a6c6c712b9ba1`  
		Last Modified: Fri, 20 Mar 2026 01:10:53 GMT  
		Size: 137.8 MB (137773162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f766ff888f40844629f073fcac0ba0f23ae5869a9ca4c0544901e8750e78ed67`  
		Last Modified: Fri, 20 Mar 2026 01:10:48 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:1434dc5f49c8d211974fca27bd2d589697ab7ccb4e54d8a7fde33f0415167ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9f30530ae4b7ee23fec926ded1912a16008d3b434d324792df3f6932719e2e`

```dockerfile
```

-	Layers:
	-	`sha256:c7f001738bb7bfd372bdfd65eab3a493c0252b56301febfbe4f074b7bcf6bf86`  
		Last Modified: Fri, 20 Mar 2026 01:10:48 GMT  
		Size: 7.0 MB (6969644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7f6f1bd3779536c4ac451036f6921770cf7dc988eff4299a462de875c1d83e5`  
		Last Modified: Fri, 20 Mar 2026 01:10:48 GMT  
		Size: 25.1 KB (25097 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:219970264d59ed70b986e5c28ae840df908a33302d270a691047bfa911ecf97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339093162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a353de414edac8e9d75ffd95d018b9d59949ad0b3a991d1b1bb05558fdc1bea0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 05:27:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 05:27:34 GMT
ENV container oci
# Thu, 19 Mar 2026 05:27:34 GMT
COPY dir:f746ef018dd3f7fba95b363c4653a5edbac791b1963bab35d68387e37854182c in /      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 05:27:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:ccda15be012570b9ee4c334e02edf875ddce34b3e788c2b4b2da3a4753faf610 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:ccda15be012570b9ee4c334e02edf875ddce34b3e788c2b4b2da3a4753faf610 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 05:27:35 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T05:26:51Z" "org.opencontainers.image.created"="2026-03-19T05:26:51Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T05:26:51Z
# Fri, 20 Mar 2026 00:01:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:01:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:01:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:01:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:01:45 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 20 Mar 2026 00:04:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:04:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:04:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:04:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:04:15 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 00:10:59 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 00:10:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 00:10:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 00:10:59 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 00:10:59 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 00:11:09 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 00:11:09 GMT
ENV GRADLE_VERSION=9.4.0
# Fri, 20 Mar 2026 00:11:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Fri, 20 Mar 2026 00:11:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 00:11:14 GMT
USER gradle
# Fri, 20 Mar 2026 00:11:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 00:11:14 GMT
USER root
```

-	Layers:
	-	`sha256:63c8858510565f2c5ca6837c562373228e6bd18c78642693e77e10422f59c586`  
		Last Modified: Thu, 19 Mar 2026 06:26:56 GMT  
		Size: 34.4 MB (34389317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52932ad68498d79edf7e415e512c223a0be61689d7a86e4d8782695524e4ae0`  
		Last Modified: Fri, 20 Mar 2026 00:02:12 GMT  
		Size: 37.8 MB (37826887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c16edf619fe70831825402cbde19e2a7dc0592e0f47403b3e523deba57a8ea6`  
		Last Modified: Fri, 20 Mar 2026 00:04:42 GMT  
		Size: 88.2 MB (88235358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a535e63e6f79160fedf6a86eb2df4978a44396f4ec9e1ec31bb7497bdffd747`  
		Last Modified: Fri, 20 Mar 2026 00:04:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd746a19bbb3eaca3ed80a259130dacb3e158b414a0e7226c01e91652ce12d3`  
		Last Modified: Fri, 20 Mar 2026 00:04:34 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569f50fb89cfb8ce39f93f58a077e0cd80ea0435c2888d33be2335a2c010b20f`  
		Last Modified: Fri, 20 Mar 2026 00:11:43 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52442f51739ec7503bbeb4f97f492e864fce8cc23ac0d1a76b0109accbffe9d6`  
		Last Modified: Fri, 20 Mar 2026 00:11:44 GMT  
		Size: 40.9 MB (40864025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcadcf7ef07707c677bca6739febe4042eb4dc97d3b634bf093e96ef48883a77`  
		Last Modified: Fri, 20 Mar 2026 00:11:46 GMT  
		Size: 137.8 MB (137773165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e0119e2c5197eaf6f1e180afd3982f6fccc1f75446e05efba36455fd83f1ac`  
		Last Modified: Fri, 20 Mar 2026 00:11:43 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:e9be9e4c38d3c7b825a3d5d39714978818a3b05b1b4f52a6be85016db759211a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6985122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08efd5e13749f4b0c654a0577f2ecd4c7fa1f1556de389315286c3932fc9e665`

```dockerfile
```

-	Layers:
	-	`sha256:f737296c286844320d35958ebdfadd2c6b5d37e21ed121209ee645f833ebe7f8`  
		Last Modified: Fri, 20 Mar 2026 00:11:43 GMT  
		Size: 7.0 MB (6960111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3dac065ac474f7fd03f88fe7023a15701ccabca4934084f4915f9b09133ecd`  
		Last Modified: Fri, 20 Mar 2026 00:11:43 GMT  
		Size: 25.0 KB (25011 bytes)  
		MIME: application/vnd.in-toto+json
