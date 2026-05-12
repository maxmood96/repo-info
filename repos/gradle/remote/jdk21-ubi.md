## `gradle:jdk21-ubi`

```console
$ docker pull gradle@sha256:3bd1eaaa3965158d714c2952cae37ec3c9d24d99926180502313c563d1ac86ed
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

### `gradle:jdk21-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:9fa02a4ba7ed159858e09ef534dd613f8e4d45d35720fc652741d085bd8dc1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.4 MB (409394884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bd5543068f167379ba749dcb137e4d0b386ffbf8bfc15109b0886745c8b2d8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:16:15 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:16:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:16:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:16:15 GMT
ENV container oci
# Mon, 11 May 2026 01:16:15 GMT
COPY dir:944b21b5e56ba1540a32a325c037508b8301ec37c6f3e20f96a07c3b3ab330c2 in /      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:16:16 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:16:01Z" "org.opencontainers.image.created"="2026-05-11T01:16:01Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:16:01Z
# Tue, 12 May 2026 00:03:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:03:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:03:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:03:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:03:43 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:05:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:05:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:05:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:05:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:05:13 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:17:25 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:17:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:17:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:17:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:17:25 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:17:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:17:29 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:17:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:17:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:17:31 GMT
USER gradle
# Tue, 12 May 2026 00:17:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:17:32 GMT
USER root
```

-	Layers:
	-	`sha256:288c81655277add7fa3f1d2c80956ecdc30e861ea53ff003f0eb7d1f488bf24b`  
		Last Modified: Mon, 11 May 2026 02:07:21 GMT  
		Size: 34.6 MB (34622430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976cadaa04549e76f7b3506abac395ce237f264ba8f7ff972e45593fc6af4ff3`  
		Last Modified: Tue, 12 May 2026 00:04:01 GMT  
		Size: 37.5 MB (37498138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecca8cb77647655ceb5833c21c2ddd6efd8c806e067002638cd889500d6dad9`  
		Last Modified: Tue, 12 May 2026 00:05:35 GMT  
		Size: 158.2 MB (158172711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c5445fdde0bc7b52cd4d4aedf80392f104596ebcd631289ba8035f36925347`  
		Last Modified: Tue, 12 May 2026 00:05:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ddb6b59eb80f4653eda5427d8a7e3d3248532874836caabba20c2dc1064d22`  
		Last Modified: Tue, 12 May 2026 00:05:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9680257a7ff44ac1053744bea0b7eed78fab2c1aa9bb84c068ce540f4950b263`  
		Last Modified: Tue, 12 May 2026 00:17:50 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c4cbaf3eb1b626b653aeda585f52293ee533a9617411cefe1672b6230865b1`  
		Last Modified: Tue, 12 May 2026 00:17:52 GMT  
		Size: 38.8 MB (38836056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ae3aaa6c4055104c75c93891b5b8b4142703e40342fd5b039b3cb5e20272b`  
		Last Modified: Tue, 12 May 2026 00:17:54 GMT  
		Size: 140.2 MB (140235901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fafae29db03cb4a5339db93726f969c7b7e17f840ef20d1b52699949dda7f69`  
		Last Modified: Tue, 12 May 2026 00:17:50 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:77a530158a01c52fd3bc7df059765b365e1d5f709fe6c0c34f63b6dafba904a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7082835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c18433d74218c7540344ef3051bbbe0b5f34f1fe2102b1d71013e1aa1122ba`

```dockerfile
```

-	Layers:
	-	`sha256:e40b9bfc6cb08bd378dac08e98bc519a13bc2311d9d9da4d82cd5cb97f51023f`  
		Last Modified: Tue, 12 May 2026 00:17:50 GMT  
		Size: 7.1 MB (7058380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6394b3f0d0f4939803d7cadb467f603c6912e8c08d9e3a335025da96977e395b`  
		Last Modified: Tue, 12 May 2026 00:17:50 GMT  
		Size: 24.5 KB (24455 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ecb7d324b49262cc3c24f2c0e012d92de0ed8163bd532be22caeeb27a7713f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.2 MB (405246212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfb30541bd85236fe05b9d9ea1f600290d2a3aa68d24ee39c97da058fd50532`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:17:49 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:17:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:17:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:17:49 GMT
ENV container oci
# Mon, 11 May 2026 01:17:50 GMT
COPY dir:c6e5c961b244885bbae5433f1eb0e567eb7e34fa66cb14c7f643fbc5449440ea in /      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:17:50 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:51 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:17:34Z" "org.opencontainers.image.created"="2026-05-11T01:17:34Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:17:34Z
# Mon, 11 May 2026 23:59:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 11 May 2026 23:59:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:59:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 11 May 2026 23:59:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 11 May 2026 23:59:44 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:03:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:03:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:03:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:03:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:03:09 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:16:40 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:16:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:16:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:16:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:16:40 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:16:44 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:16:44 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:16:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:16:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:16:47 GMT
USER gradle
# Tue, 12 May 2026 00:16:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:16:48 GMT
USER root
```

-	Layers:
	-	`sha256:b0d48ca6ae597735e3215ce3085802fb19010a7e5256d1d09af0257d955c5185`  
		Last Modified: Mon, 11 May 2026 02:10:59 GMT  
		Size: 32.7 MB (32747172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e535de146c71409c11cf88a63583572bd33e66987e6acf72dee80eb746c5b27`  
		Last Modified: Tue, 12 May 2026 00:00:08 GMT  
		Size: 37.4 MB (37444321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392a2686044fee0ada94c1dd4d8eea298773bd5fb944f59b0234e7c1fe5476de`  
		Last Modified: Tue, 12 May 2026 00:03:30 GMT  
		Size: 156.5 MB (156464398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4502211045bd5de7d3de0a3ba84ca695f24b4650aa8d58eb869df366209c9e31`  
		Last Modified: Tue, 12 May 2026 00:03:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942875047dfaa4c900ced58665fac899818215d5f249ab42c855b373919f479d`  
		Last Modified: Tue, 12 May 2026 00:03:25 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89ba30602395e0e8fd228a8897ad367c21b4228e5c5109e935af2dab2ac0be9`  
		Last Modified: Tue, 12 May 2026 00:17:06 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c871b657aeadf98d19d7c515e68110e2009d2ab4c41314b472386328cc529f0`  
		Last Modified: Tue, 12 May 2026 00:17:08 GMT  
		Size: 38.3 MB (38321045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba200453cfd25ba5fbac46a2c5b091ceb697caa6f589632643e2f36780227041`  
		Last Modified: Tue, 12 May 2026 00:17:11 GMT  
		Size: 140.2 MB (140235899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a54bff40a4f75c62915cd6f69bc94a586290f1b112c92f638ceed7f793a765`  
		Last Modified: Tue, 12 May 2026 00:17:06 GMT  
		Size: 29.3 KB (29340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:40a8404114e5a40f303f0f900238921b4a4788cea3974e74403b6758b3bf8d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02813aa0e37349416d912f605d28a8773394bdd313bb76689d2611e7874cd6f6`

```dockerfile
```

-	Layers:
	-	`sha256:eb06217e1e3a4cf8a7452936628580daf9aa3e8d88da624e96699745ac17cbb0`  
		Last Modified: Tue, 12 May 2026 00:17:06 GMT  
		Size: 7.1 MB (7056636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2c0e1cbc289d34e1cbb8518ff40cb6d11f101e48b0096ea68de2e984ff9c51`  
		Last Modified: Tue, 12 May 2026 00:17:06 GMT  
		Size: 24.7 KB (24651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:5e517c21619032f1d0c5f4aa835f0e7fc50440d119caedba8421afdaf0dc3d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.2 MB (417173676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564564f8a7dc000076b96d1e8e4744691161615edafbeb85d1ea6ee6f3450882`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 09:10:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:10:53 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:10:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:10:53 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:10:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:10:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:10:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:10:53 GMT
ENV container oci
# Wed, 06 May 2026 09:10:53 GMT
COPY dir:158c3f0cb7ce24639f61426b68518af6eac4aaf0de71f58d18f634631d8ec0f0 in /      
# Wed, 06 May 2026 09:10:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:10:53 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:10:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:fa10e966ee7289b238e615643b46ea2d8e307515115a0ea9e2b102df79fabf33 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:fa10e966ee7289b238e615643b46ea2d8e307515115a0ea9e2b102df79fabf33 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:54 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:10:41Z" "org.opencontainers.image.created"="2026-05-06T09:10:41Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:10:41Z
# Fri, 08 May 2026 16:18:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:44 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 16:24:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:24:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:24:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:24:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:24:57 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:40:42 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:40:42 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:41:21 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:41:21 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 16:41:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 16:41:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:41:27 GMT
USER gradle
# Fri, 08 May 2026 16:41:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 16:41:29 GMT
USER root
```

-	Layers:
	-	`sha256:8fabb2dd484322746fc4d1ed7e1fbca1a0509bc14f76029832e436bbc2825a8d`  
		Last Modified: Wed, 06 May 2026 12:15:25 GMT  
		Size: 38.8 MB (38751685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b7c362fde3ba2e4cb3c58a05618ebaafb430e3fbe1631353247827620d8d0d`  
		Last Modified: Fri, 08 May 2026 16:19:23 GMT  
		Size: 39.3 MB (39256885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baf38f93e1243b1ca3215ee2789605ef7b13b5fba1134086cc474519ece2148`  
		Last Modified: Fri, 08 May 2026 16:25:38 GMT  
		Size: 158.3 MB (158348540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff08625fff91d084eef5517739f1640e55d159cf4452cc60930a3ffbf93bc1`  
		Last Modified: Fri, 08 May 2026 16:25:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a201bde476dece79e2e6e047fd0eb7acbc1dd7c5f19adc9169bc8b0ee55d2a0d`  
		Last Modified: Fri, 08 May 2026 16:25:34 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4124c0fed0e3e6caa827cc9dc6e449467255092d1aef88669d8c5ddf077e61b3`  
		Last Modified: Fri, 08 May 2026 16:42:30 GMT  
		Size: 1.6 KB (1590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eda8f82a935e91dd5f601fd1c4e83ac454ba45af55414c44e55a2f9db190aa6`  
		Last Modified: Fri, 08 May 2026 16:42:32 GMT  
		Size: 40.6 MB (40576204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290027ff21b66b3cc9fc56c598f63c2226dd2f74648150de9e1490c0fee79a97`  
		Last Modified: Fri, 08 May 2026 16:42:34 GMT  
		Size: 140.2 MB (140235942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838376412410f0c7a2aa4402dd2813d0d379ee18344ec2aa92338dabb773963`  
		Last Modified: Fri, 08 May 2026 16:42:29 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:d9ad6f281f077e0ab934f942b098e20eec4e8180e92ba321a15eec31f32f461e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7074325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a975a137bb85f90cf995fa76971ec97dc15cd9c8162794c6add5bbcb9cdd2`

```dockerfile
```

-	Layers:
	-	`sha256:ea7c22af2132c380697278069aa0e9d7bd8dc8a5c8961190301d75c02c010e1a`  
		Last Modified: Fri, 08 May 2026 16:42:30 GMT  
		Size: 7.0 MB (7049798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f426126c4f12b088a2f57f51cd7e68ff569a267f26aad790b6d513b4121b9fb`  
		Last Modified: Fri, 08 May 2026 16:42:29 GMT  
		Size: 24.5 KB (24527 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:75760239d22ee4cf7adf5d7131bf92cd0f28eed0d2cd6c652392d9958ecf090f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 MB (400886488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e35e716b06b486f214fbb37549122d447a77ccbdf3796d62c872a565cb28a93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:23:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:23:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:23:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:23:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:23:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:23:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:23:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:23:16 GMT
ENV container oci
# Mon, 11 May 2026 01:23:17 GMT
COPY dir:0579bc85c05b217dd77b2ce225f64d3cb10f81a6a3726b91387ffbc978d6e453 in /      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:23:17 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:23:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:81f827a1784652793e747198fea65ce1ad402e9b3c1587adce62db262e60fb88 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:81f827a1784652793e747198fea65ce1ad402e9b3c1587adce62db262e60fb88 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:23:17 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:22:36Z" "org.opencontainers.image.created"="2026-05-11T01:22:36Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:22:36Z
# Tue, 12 May 2026 00:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:00:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:00:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:00:39 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:02:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:02:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:02:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:02:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:02:18 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:12:48 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:12:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:12:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:12:48 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:12:48 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:12:52 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:12:52 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:12:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:12:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:12:57 GMT
USER gradle
# Tue, 12 May 2026 00:12:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:12:58 GMT
USER root
```

-	Layers:
	-	`sha256:c8191d3132a8f64ba77e2e7e35ea28fba961048b0be562036986e4b4138e5000`  
		Last Modified: Mon, 11 May 2026 06:17:00 GMT  
		Size: 34.4 MB (34447893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbb67b875402a07d4d37d60a9c04f86b7bb89be6c15373d36cf06b6b31221fb`  
		Last Modified: Tue, 12 May 2026 00:01:10 GMT  
		Size: 37.9 MB (37883242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea07dd9e55bfbb256bff139d80f150c1b431ff522c3d936c17bd43f6d34bb98`  
		Last Modified: Tue, 12 May 2026 00:02:45 GMT  
		Size: 147.4 MB (147390185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137708bee83ef122b4d66345511132ba988e6b979ad2de55f506b6c639518083`  
		Last Modified: Tue, 12 May 2026 00:02:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8137005b72e476419d64e1aa73ab87e6702b31836bbc8c9ffa452fe14ccec1f6`  
		Last Modified: Tue, 12 May 2026 00:02:36 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec08d7894d1bc92ac7a6cde4aada115248e15402bafd9733bbab0cb4d451911`  
		Last Modified: Tue, 12 May 2026 00:13:28 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29c9c0ac4ea9a67888e78ff7dc0391d468d175edd01701ff46e823f0ad513b3`  
		Last Modified: Tue, 12 May 2026 00:13:29 GMT  
		Size: 40.9 MB (40924864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9279ae9a87e563c7cc3ac38745d9a6a6fd96a5939fc85b88e1edae43a2a152d`  
		Last Modified: Tue, 12 May 2026 00:13:31 GMT  
		Size: 140.2 MB (140235897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a360bf704c4177f5d690d59b630b056abf71412b9e99f450fc6f8450cbebc238`  
		Last Modified: Tue, 12 May 2026 00:13:28 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:dd138b2dd1167c0ce7b962a8d7d0f40d2af1b8f2e6a48eee595a834c8afb857f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7063480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8d66c887a141d3cbccc46ab514449b839fe50b5d899627b036f95a3b547669`

```dockerfile
```

-	Layers:
	-	`sha256:3db6ee77beb3204aeea6c62e2e4322c209efe56bae88613d4e361efd26c7186e`  
		Last Modified: Tue, 12 May 2026 00:13:28 GMT  
		Size: 7.0 MB (7039027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fca327231e264dedf060fa197213684d62c29f401ffeb4a812601f71128055b`  
		Last Modified: Tue, 12 May 2026 00:13:28 GMT  
		Size: 24.5 KB (24453 bytes)  
		MIME: application/vnd.in-toto+json
