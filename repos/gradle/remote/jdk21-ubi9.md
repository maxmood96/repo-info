## `gradle:jdk21-ubi9`

```console
$ docker pull gradle@sha256:4e45a6cf50aabec0ce257a1ecdd7a6f0dddcbfc393247306cb852feda742e932
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

### `gradle:jdk21-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:cde941a1e4cde7415a4ce23d9531a33ee65ae5cbe42cc25c63a8a878af83e633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.3 MB (408304769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f613f6c815aeeb06da87b7a96f9d08dd52f9ce3f598ef77bd1ab8e5bd42292`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:10:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:10:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:10:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:10:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:10:52 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 30 Jun 2026 00:11:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 30 Jun 2026 00:11:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:11:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:11:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 00:11:45 GMT
CMD ["jshell"]
# Tue, 30 Jun 2026 01:10:20 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:10:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:10:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:10:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:10:20 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:10:23 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:10:23 GMT
ENV GRADLE_VERSION=9.6.1
# Tue, 30 Jun 2026 01:10:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Tue, 30 Jun 2026 01:10:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:10:26 GMT
USER gradle
# Tue, 30 Jun 2026 01:10:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 30 Jun 2026 01:10:27 GMT
USER root
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741c9b0f64bf14f3bec31c4a81d3ac0928616418a573159f3ec31f1f7209ca08`  
		Last Modified: Tue, 30 Jun 2026 00:11:08 GMT  
		Size: 30.9 MB (30877611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49878acb3585816bfebed190e8efa8a63232d6dc8ec5fc7fe312b7169d760e77`  
		Last Modified: Tue, 30 Jun 2026 00:12:05 GMT  
		Size: 158.2 MB (158172681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e053e47ede82d56450135625fd51642d4dad46e21fd24b12e0fbacebca681`  
		Last Modified: Tue, 30 Jun 2026 00:12:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5be73217becd80a22ceb85af44f0e2f1b1bce841fa0bc42141e604e98fa485`  
		Last Modified: Tue, 30 Jun 2026 00:12:02 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648e644efb78d23b58bfd763f1721591035e43a631e4c9a08698e847986ba5b9`  
		Last Modified: Tue, 30 Jun 2026 01:10:45 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5240e5397aad652c8b0cc45aafcd1bf49d79d5135627d6081a0731291fe3a422`  
		Last Modified: Tue, 30 Jun 2026 01:10:47 GMT  
		Size: 37.9 MB (37941863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d613c10e9f6b3e1ca95c89f2d4b4b37878620183b7d62de143774f7c0fd1675e`  
		Last Modified: Tue, 30 Jun 2026 01:10:49 GMT  
		Size: 140.6 MB (140596023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a8bcca01395df8b157d2c2e23c594fd3d56a3c5107fbc3c87de9a6693966`  
		Last Modified: Tue, 30 Jun 2026 01:10:45 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:2dd2e4a6b562f68140b2e1b33110fe7da79f26015c4fc67007475272c8c4e227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c433329727060ab00c322e580e185e24ee9e82cb1b31d1c279ce8786c26849b8`

```dockerfile
```

-	Layers:
	-	`sha256:05d7b9c44f9953e2418ead875a026c478c685b242e331dcd0c0e63763f8efe31`  
		Last Modified: Tue, 30 Jun 2026 01:10:45 GMT  
		Size: 5.4 MB (5435128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8550f5ba33efd89e25a0ed361addd2dd0fdcda1bdce536c77efb6a2c0a63c480`  
		Last Modified: Tue, 30 Jun 2026 01:10:44 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3daff1771e1248eff96b5bc117cd138acf6a8053d1ed399f8d25b927637a4c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.9 MB (403934853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a1f30e07191822fd13c3ffc11ca26b146d8a1cd27266131f516c534f5e29e8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:09:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:09:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:09:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:09:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:09:15 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 30 Jun 2026 00:10:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 30 Jun 2026 00:10:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:10:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:10:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 00:10:12 GMT
CMD ["jshell"]
# Tue, 30 Jun 2026 01:10:23 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:10:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:10:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:10:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:10:24 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:10:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:10:27 GMT
ENV GRADLE_VERSION=9.6.1
# Tue, 30 Jun 2026 01:10:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Tue, 30 Jun 2026 01:10:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:10:31 GMT
USER gradle
# Tue, 30 Jun 2026 01:10:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 30 Jun 2026 01:10:31 GMT
USER root
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c609dcbef36918d198f81c35e8f83dfa4f97ee71e4867f46913b3e81183289f6`  
		Last Modified: Tue, 30 Jun 2026 00:09:34 GMT  
		Size: 30.8 MB (30794487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6131f7168ca07bd9aa4d384f3fb90ac80bdec05931d9f47b3436184f261d8a41`  
		Last Modified: Tue, 30 Jun 2026 00:10:32 GMT  
		Size: 156.5 MB (156464362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e368ccbedc32c08ce86cedd8b52b9b3e247dcb50b7fb295cc808311d304090a3`  
		Last Modified: Tue, 30 Jun 2026 00:10:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25009e60fd0d281c0823181910b2743c1c5c5bc46b00317176a7948676c9171`  
		Last Modified: Tue, 30 Jun 2026 00:10:28 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78c6a161ec6c88f6a8a6ac272b77d8cfc5737cb7e509b54dc8a9b19a1267c11`  
		Last Modified: Tue, 30 Jun 2026 01:10:48 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537daa6b53e816425940f35446250631303ddbc898457659b996200a0613ca71`  
		Last Modified: Tue, 30 Jun 2026 01:10:50 GMT  
		Size: 37.2 MB (37227032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67509436c54b0b95e5c5ef7ba0b9c077f7a48678c28c1c54b10a26778174eec4`  
		Last Modified: Tue, 30 Jun 2026 01:10:53 GMT  
		Size: 140.6 MB (140596027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d416e86c4ecded9f0cbfad4b6a387c33dbf8f6fd52cd83a14ac803f8bfcfd62`  
		Last Modified: Tue, 30 Jun 2026 01:10:48 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:08a121692c01055e6ce08120b23ad658af168c717887ccbc763c78c0a9f54f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6baa20ce9ae653984d2e1b17815b68998b99f4fd290a3fbad8069189a68c3e98`

```dockerfile
```

-	Layers:
	-	`sha256:de8a9842a7cd720945f4b7bab8bd5661626e429164ff8a8839e95086be676f79`  
		Last Modified: Tue, 30 Jun 2026 01:10:49 GMT  
		Size: 5.4 MB (5432740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3760c1736e5a4546aa0dccfb0d01e79938abf27f0aab37ca0686d42bf458ec4`  
		Last Modified: Tue, 30 Jun 2026 01:10:48 GMT  
		Size: 23.7 KB (23654 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:495829506574444b8274ec89a91ebc7e3ede3ba846d73ecdead7d0fab569f562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.3 MB (413301795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b936b1c8a1beef922f0a2085398b370c0c21f0acab732aa0702af92b84e2af`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:43 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:4c1c925f52e2bf94f6f51ed2040707135dad2469062fae485083f1e3880aa690 in /      
# Mon, 29 Jun 2026 04:51:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:44 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:b37bcc35410383d4962d130d7f52524a29de2416d65cdbb7496d3441baade925 in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:b37bcc35410383d4962d130d7f52524a29de2416d65cdbb7496d3441baade925 in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:44 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:51:26Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:51:26Z" "architecture"="ppc64le" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:51:26Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:11:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:11:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:11:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:11:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:11:34 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 30 Jun 2026 00:14:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 30 Jun 2026 00:14:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:14:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:14:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 00:14:14 GMT
CMD ["jshell"]
# Tue, 30 Jun 2026 01:08:46 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:08:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:08:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:08:46 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:08:46 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:09:01 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:09:01 GMT
ENV GRADLE_VERSION=9.6.1
# Tue, 30 Jun 2026 01:09:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Tue, 30 Jun 2026 01:09:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:09:06 GMT
USER gradle
# Tue, 30 Jun 2026 01:09:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 30 Jun 2026 01:09:07 GMT
USER root
```

-	Layers:
	-	`sha256:cab5e0c171012774531d882f585d3be1eb8a97b88a5126afe48b35169caafc50`  
		Last Modified: Mon, 29 Jun 2026 06:11:46 GMT  
		Size: 45.1 MB (45078234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3383a7a24164308cd34dd0b3f319e45e2be49008abc404e48fcc73abdb8e02b0`  
		Last Modified: Tue, 30 Jun 2026 00:12:08 GMT  
		Size: 30.1 MB (30082685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eec37042b466d1bca62f78864452c0506f911747000a3d6d4ee7768db59d0e`  
		Last Modified: Tue, 30 Jun 2026 00:14:50 GMT  
		Size: 158.3 MB (158348478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10c3533ef2122889a17703a434a8b84970c2cd9f2d29ad3a9344fa65c2e4178`  
		Last Modified: Tue, 30 Jun 2026 00:14:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8336197a02d4dff6670a0d53874c6e9de628ff37cfb2328b052f563990c89a6`  
		Last Modified: Tue, 30 Jun 2026 00:14:45 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248f5ce403f4a5498755f3e54d8525f797bf9c19caf90dda637b8c8456c328af`  
		Last Modified: Tue, 30 Jun 2026 01:09:43 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9864efc1cc4796fbec1152c9bc747b16b7240eba5de5b6a5cbd0f027586c8456`  
		Last Modified: Tue, 30 Jun 2026 01:09:48 GMT  
		Size: 39.2 MB (39191828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a60cf0922420e442b904e698a18995cd2538941c08a30569911d14d32a9592`  
		Last Modified: Tue, 30 Jun 2026 01:09:53 GMT  
		Size: 140.6 MB (140596026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b410c189ce4c466798f17c66017ee7845e1a041446ff87890c60ffc1b98609`  
		Last Modified: Tue, 30 Jun 2026 01:09:44 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:40b7f64283681b5485e8a63b18e1c7923124a7fca9d031ee205eda43e4a2d13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9c9812ae8b6f08cca4b27b3fddca1db107e9fd26dd2900bc87234d0ebedd8f`

```dockerfile
```

-	Layers:
	-	`sha256:fb92628a4409b6edea9ac3b13d3d6ef3d354c07af34f2a1cb2047b0005446a61`  
		Last Modified: Tue, 30 Jun 2026 01:09:44 GMT  
		Size: 5.4 MB (5430701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731501f7fcf50848db1dc1bc4be109df485b590385099b854d8671c9cd9ea27e`  
		Last Modified: Tue, 30 Jun 2026 01:09:43 GMT  
		Size: 23.6 KB (23584 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:6dfef1c6e8b3d69be31e8c38db6271a14b69acfa601f62d46d86f35a1490c036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.7 MB (394698721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f49ac3dc2bbc794f40e1c310be798d0cf72ce22c402c40a509c946b166f1d68`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:54:01 GMT
ENV container oci
# Mon, 29 Jun 2026 04:54:02 GMT
COPY dir:bef74dcd4da475c586b5111f5945e8f6c9f80ccf9a44e3148ec57db13ecb6f76 in /      
# Mon, 29 Jun 2026 04:54:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:54:02 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:54:02 GMT
COPY dir:b86703d2983643457ac1d15b6653c2433af6c84ce9ec066326faf8d778c83033 in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:54:02 GMT
COPY dir:b86703d2983643457ac1d15b6653c2433af6c84ce9ec066326faf8d778c83033 in /root/buildinfo/      
# Mon, 29 Jun 2026 04:54:02 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:53:12Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:53:12Z" "architecture"="s390x" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:53:12Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:09:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:09:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:09:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:09:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:09:34 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 30 Jun 2026 00:10:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 30 Jun 2026 00:10:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:10:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:10:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 00:10:21 GMT
CMD ["jshell"]
# Tue, 30 Jun 2026 01:08:57 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:08:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:08:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:08:57 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:08:57 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:09:06 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:09:06 GMT
ENV GRADLE_VERSION=9.6.1
# Tue, 30 Jun 2026 01:09:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Tue, 30 Jun 2026 01:09:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:09:10 GMT
USER gradle
# Tue, 30 Jun 2026 01:09:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 30 Jun 2026 01:09:10 GMT
USER root
```

-	Layers:
	-	`sha256:2b76546ac3454fac1865108cd9899827c06545a83bd476481d8bd3017de72774`  
		Last Modified: Mon, 29 Jun 2026 06:11:36 GMT  
		Size: 38.8 MB (38768635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47c019bbc5bf5fafae88fde703fb08f23e7357ff980fee2471235e2e7902fb1`  
		Last Modified: Tue, 30 Jun 2026 00:09:56 GMT  
		Size: 30.4 MB (30413888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b3dd545f084c859fde8854929b6f5300e7f6cb545af3f60b2b81e64b6a4a2c`  
		Last Modified: Tue, 30 Jun 2026 00:10:47 GMT  
		Size: 147.4 MB (147390180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afff3d805d04e030c3a57b38688851a7a1aa7159a53a6c07a69544ccc9a8915`  
		Last Modified: Tue, 30 Jun 2026 00:10:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f955e95467f88d7ccc7a51284eb13cbbd12d6abc2803165943196d4ed62c7118`  
		Last Modified: Tue, 30 Jun 2026 00:10:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee7951a606faf4a745820d4a956392c57bffacfa1b85c5f5b693fb7860641ed`  
		Last Modified: Tue, 30 Jun 2026 01:09:35 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa561a6cb76b11856bb67d3d8dc2048c16893e4c45a3ad87fcd47669333f7b1`  
		Last Modified: Tue, 30 Jun 2026 01:09:36 GMT  
		Size: 37.5 MB (37525458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3225c42c0daf7fcd7c3a15e4dc749fc0475f29b1ed4ce9e1585e209595b9ab`  
		Last Modified: Tue, 30 Jun 2026 01:09:38 GMT  
		Size: 140.6 MB (140596025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7e430ca8242a169f3df8bafeb88c0382f9bc772b601eb7c12f9dfec72c2ba8`  
		Last Modified: Tue, 30 Jun 2026 01:09:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:24ca0096395abbe397222f925abcdf9784e2aba77a1a1df1b6cdcc5c38690cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729ba02b4fc8630deaab7da545d93052ee0acefddb77ef6c776785613145a8d2`

```dockerfile
```

-	Layers:
	-	`sha256:e3be5935eb7275f6bccae07986efa86f5410b840c47f01edb08172e1d69b406b`  
		Last Modified: Tue, 30 Jun 2026 01:09:35 GMT  
		Size: 5.4 MB (5419951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59120b2e9d0c67ceadbd18f0ae7bcfe61c2fcdee1279513da23cf629d4dace4d`  
		Last Modified: Tue, 30 Jun 2026 01:09:35 GMT  
		Size: 23.5 KB (23528 bytes)  
		MIME: application/vnd.in-toto+json
