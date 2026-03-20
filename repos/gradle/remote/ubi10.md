## `gradle:ubi10`

```console
$ docker pull gradle@sha256:32db2f6ae7ec7418e48c94421a7fc82f025dcec1dde3e7c5234a2ace248c2572
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

### `gradle:ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:f8fafd63c3381b4d8a0efa1a7884aebf6aeb77244f3d8a8b9cfaaf5d2de80d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340912635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f538164f548ea7de35f10ec1f1d79012586bd4793b4a3389262950c7e99aaf7a`
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
# Fri, 20 Mar 2026 17:09:58 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:09:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:09:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:09:58 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:09:58 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:10:02 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 17:10:02 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:10:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:10:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:10:04 GMT
USER gradle
# Fri, 20 Mar 2026 17:10:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:10:05 GMT
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
	-	`sha256:d7646d6981358fee227103fafd855c583eeeae6eeb5b1eaf7ce2a55a6bed34ff`  
		Last Modified: Fri, 20 Mar 2026 17:10:22 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503ae02766742a6af90504e60da39c479ed8df765c30d5a96444a7af13c7ff38`  
		Last Modified: Fri, 20 Mar 2026 17:10:24 GMT  
		Size: 38.8 MB (38758843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612af5aeadfc5d993b6a0f509d77c0b154b897b57feb7815021e3b46abd459db`  
		Last Modified: Fri, 20 Mar 2026 17:10:26 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a1212906781313089c68741c87890285cedafd54779639a09a49478d4b6155`  
		Last Modified: Fri, 20 Mar 2026 17:10:22 GMT  
		Size: 25.6 KB (25626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:3ad4840e617c4c7d3169549d3e746a4122f7dfd9710789cb80161ce0dc99ad2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3ba1f736e9f11674a8539df8e98ce7d3c9194f8d2aba9cfc3c7fb465d663c4`

```dockerfile
```

-	Layers:
	-	`sha256:d74d2f0693cd28018cc02d7cd110f554383770fae511a06fe19cca37ae069148`  
		Last Modified: Fri, 20 Mar 2026 17:10:22 GMT  
		Size: 7.0 MB (6994902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dab289fbccdac52913c999d39548e26a0ba2774b422a7b4544f33dddfa7b0c`  
		Last Modified: Fri, 20 Mar 2026 17:10:21 GMT  
		Size: 25.0 KB (25013 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9bce1571fa830f4fb29197315210573c3b0aff2bb2217fd95c41874b1a73365e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337460325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301036e8bd7b6eebf57c5eb7404161b5fc9ffc46f052aefc4d24c9fed4c1ca23`
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
# Fri, 20 Mar 2026 17:09:55 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:09:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:09:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:09:55 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:09:55 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:09:59 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 17:09:59 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:09:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:10:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:10:02 GMT
USER gradle
# Fri, 20 Mar 2026 17:10:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:10:03 GMT
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
	-	`sha256:2d8f830fd23d273da9ff90f8c2824d387d8cbe59a6a4da7ec0e52836b56d5cc6`  
		Last Modified: Fri, 20 Mar 2026 17:10:21 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5953ca75e6f5893ab84fb5596386c4ad827cab5109114101c444bf5c944c5369`  
		Last Modified: Fri, 20 Mar 2026 17:10:23 GMT  
		Size: 38.3 MB (38254442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8d1c79117d1990199ce9eaed42f39ee41a41e075006b1f9517e5902e71957d`  
		Last Modified: Fri, 20 Mar 2026 17:10:26 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addd73cb61e57b51b638f1206800f104a1afcda3e9dadb14a8835182949c6e9b`  
		Last Modified: Fri, 20 Mar 2026 17:10:21 GMT  
		Size: 29.4 KB (29351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:b5f44add30364f10085c76dc6e5d33a296c722d3362a9615578465b20718dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7018413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e641e20d423650a432098764c390f786db272171a3919d89ba2eb5c06ec6f0b`

```dockerfile
```

-	Layers:
	-	`sha256:d07737f4bdac6a4ce960321588c3de229e0d3b77ff58b9fe3de15131c0fa686e`  
		Last Modified: Fri, 20 Mar 2026 17:10:21 GMT  
		Size: 7.0 MB (6993179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82379e2681746d30db620fe0f66f8a77b2f7ccf8e46d7cf6c545a2cab426c529`  
		Last Modified: Fri, 20 Mar 2026 17:10:21 GMT  
		Size: 25.2 KB (25234 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:450bfaaa55fef866a8db641a2645c5a73a97f52e8c555e4387d5d9767ae3d286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347882711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c36de1a14800f69eeafb14a46acbbe74dfb8294fb9285e0aece61b30a22da0`
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
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 01:09:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:07:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:07:32 GMT
USER gradle
# Fri, 20 Mar 2026 17:07:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:07:33 GMT
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
	-	`sha256:f8f5bae06b2d703620f736eec15cbb0379874709085b4bc3bd14e2bd26fdfd1e`  
		Last Modified: Fri, 20 Mar 2026 17:08:09 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e743bf3231f494535be3bfe8732fd0d42afc1d31bd178ebdbeb56ed705ac07`  
		Last Modified: Fri, 20 Mar 2026 17:08:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:442efb471dfccbb208433c77469e0488311d87c90b78c45ddc515315de501196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2366120acc46f419358e40874f31e1817296665492be542ec826ca84360f5f5`

```dockerfile
```

-	Layers:
	-	`sha256:3dfe6bbdca43d974ecb8c94fb8f270f56ea50cb70ab9d61951c143e4587fe4ef`  
		Last Modified: Fri, 20 Mar 2026 17:08:05 GMT  
		Size: 7.0 MB (6969644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68065d0671b9c521486b673a5971cffc56ef68ad3749197e4d50da866d21b62`  
		Last Modified: Fri, 20 Mar 2026 17:08:05 GMT  
		Size: 25.1 KB (25097 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:50028fbe34f180bf5097f9ef647f5bdc20a150f14ab1bca52504a9323c605e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339128342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e93f8a9d3edc5aeb270216a6f9711bf4a7859f9094e9127a2f28c5b1b56e4d`
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
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 00:11:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:07:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:07:54 GMT
USER gradle
# Fri, 20 Mar 2026 17:07:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:07:54 GMT
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
	-	`sha256:5f6cbb533548944b187770f7d8346ca4da745295803b4f11b6b4a097a975fd4b`  
		Last Modified: Fri, 20 Mar 2026 17:08:24 GMT  
		Size: 137.8 MB (137808340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3876a140cfaa12a66bb7c16a0419a7a35c8ef409ec1191d0627221509311de5e`  
		Last Modified: Fri, 20 Mar 2026 17:08:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:0a196f528e5f268efaba1e3bbc4eac7016bf255b134b8eb8f94544e7a39e45f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6985122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c2ceb17eb649443f23ffc4caf7c7c4ae5184e05155ffbda63951b568c9db32`

```dockerfile
```

-	Layers:
	-	`sha256:e48ba8173fc962caadd67220484f7ffad8c106b6b0bad75ab9369da72d2713c2`  
		Last Modified: Fri, 20 Mar 2026 17:08:22 GMT  
		Size: 7.0 MB (6960111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d11a0a0b90543c6fa9a51077f842bed2db46bfd107665dde9684d170e1a327ad`  
		Last Modified: Fri, 20 Mar 2026 17:08:22 GMT  
		Size: 25.0 KB (25011 bytes)  
		MIME: application/vnd.in-toto+json
