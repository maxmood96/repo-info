## `gradle:jdk21-ubi9`

```console
$ docker pull gradle@sha256:8244b3355c1007a9834158895e1e175e512e214395285a2c966475cc4f03e7dc
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
$ docker pull gradle@sha256:9919bc94b211b84cf0262a4ccac2ad26b07b905eb21020fedd3eb91b40afc51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.1 MB (405068761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beff82bff7f1dda6291ab666e65c469076973987096811b2b6870ec3f3b96068`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:26:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:26:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:41 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 25 Jun 2026 23:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:27:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:27:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:27:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:12 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:11:57 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:57 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:57 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:12:01 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:12:01 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:12:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:12:04 GMT
USER gradle
# Mon, 29 Jun 2026 17:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:12:04 GMT
USER root
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37515b7623a771c7568760216381f554109116907c31a04202c053b1884f7b7b`  
		Last Modified: Thu, 25 Jun 2026 23:26:57 GMT  
		Size: 27.7 MB (27660374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806210370cfa220ec46c57654623aa9a306fe555e28c8eb07f5e4d39a834e8ee`  
		Last Modified: Thu, 25 Jun 2026 23:27:30 GMT  
		Size: 158.2 MB (158172662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef6856fe1cdc15a7ceefdbf26dfbad839e96c13f75a51a0fd70c52871e9d8e7`  
		Last Modified: Thu, 25 Jun 2026 23:27:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1181defc44b2c5755cddf86669d267116513261ec1177d9e6135478497217f0b`  
		Last Modified: Thu, 25 Jun 2026 23:27:17 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ff888e5086f215c9e092682cb4674412920c76f6bd6e5583123230b9558787`  
		Last Modified: Mon, 29 Jun 2026 17:12:21 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eb596852b66b3128b2eac1fda260481715389d2dffd282498ec179e129045c`  
		Last Modified: Mon, 29 Jun 2026 17:12:23 GMT  
		Size: 37.9 MB (37920699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d698596d59270fd66bf441d73f4b3cc3f7977dc741edb749e1b4acc6fbf640`  
		Last Modified: Mon, 29 Jun 2026 17:12:25 GMT  
		Size: 140.6 MB (140595975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e3428a81c0f053341a838be1faf311013ce2eedf20488117d85eb912cc758`  
		Last Modified: Mon, 29 Jun 2026 17:12:21 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:4c3faf26acdd9db42c94b6e5ae9395d4730f8f6941255ad5ca0643c6241c2491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e8e491dc027b46b163bf068408ce635ec8809b5c89643a500d7d59e3f1f3a8`

```dockerfile
```

-	Layers:
	-	`sha256:fd65c92ea54cd5f7b8056b293c1f1232d0c7ba1cce7f5de53ed267ab3c53a352`  
		Last Modified: Mon, 29 Jun 2026 17:12:22 GMT  
		Size: 5.4 MB (5435120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc65003bb485a7853973bf904d7f0cd97f86c39774913d00c94084bb2b216d31`  
		Last Modified: Mon, 29 Jun 2026 17:12:21 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:120afec38dc54de2248bd856b807c8a4dca59e94413502040ed6e568267728a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401216352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638c02f34d9ca58746202a38f66d12483692fa204a8ee61e7f7d7e020c638f57`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:26:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:19 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 25 Jun 2026 23:26:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:26:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:26:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:26:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:29 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:12:00 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:12:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:12:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:12:00 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:12:00 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:12:04 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:12:04 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:12:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:12:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:12:06 GMT
USER gradle
# Mon, 29 Jun 2026 17:12:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:12:07 GMT
USER root
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061428a206623bdde594b4a9bf4bb8b3d849480a82ac9be3cf550875a95c420`  
		Last Modified: Thu, 25 Jun 2026 23:26:47 GMT  
		Size: 28.1 MB (28100474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595c47e9af9f95e1ded11cf855c772c5745b5aae93b6b6830ee88182a6e83c0c`  
		Last Modified: Thu, 25 Jun 2026 23:26:50 GMT  
		Size: 156.5 MB (156464332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870983f7fffcc735d520000175e686a197cc31851dafedc8844a0d362f86d038`  
		Last Modified: Thu, 25 Jun 2026 23:26:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f540a71e558f3c5eb70c185319d9f748dd4ec3295157f5461c6b878bdbf4086a`  
		Last Modified: Thu, 25 Jun 2026 23:26:46 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fbeeaecc60bf27bd516b1f50b8ee12df74a04bdaf559a10166e861680009e`  
		Last Modified: Mon, 29 Jun 2026 17:12:24 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b5c9c80cdc35b3d50411a7a4128611cf5051478dd1b34b014632332d2b0165`  
		Last Modified: Mon, 29 Jun 2026 17:12:25 GMT  
		Size: 37.2 MB (37203887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b2c67894b16230fc3b4e5f691a8e5019045de5ced4d439d110db739dc7f631`  
		Last Modified: Mon, 29 Jun 2026 17:12:28 GMT  
		Size: 140.6 MB (140596027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d333818b16e831a91a4eda3a425bc8a4a0d57cfbd1bb67384dd074108c2348`  
		Last Modified: Mon, 29 Jun 2026 17:12:24 GMT  
		Size: 29.4 KB (29352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:6d90cba8221bdbe95768ccccc7138b09acf34f418c6670b5096b6f87ab4207c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44b53e0df81d37d80378f59c111708ae34c7162e6034535f1e19d82962039f4`

```dockerfile
```

-	Layers:
	-	`sha256:772df6e99f6dfa86cd67b71a68efd6f42f9ba19c3b5df94f4523760aa1035a70`  
		Last Modified: Mon, 29 Jun 2026 17:12:24 GMT  
		Size: 5.4 MB (5432732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0579060ba8617315f0b26cc971c6d33f60c250e9af5e8dc8a47699e7671c79d`  
		Last Modified: Mon, 29 Jun 2026 17:12:24 GMT  
		Size: 23.7 KB (23655 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:0516091278bd9b5df9817f3f8b07fe388d29324879b16b69d181d5569b219f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.3 MB (413307969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aac47ffbcb962dd509fc94eff805e47a2faa5bbb652642fe9cd6b9abe17d7e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:04 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:f90c99a59bd474ed6a51399eee7df05393563fdaaa902130421d08a1a3fedeec in /      
# Thu, 25 Jun 2026 05:49:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:05 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:cb70b1c584e490eac8673058fb514f718bb38524b957a3c5934b6749eca2ca95 in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:cb70b1c584e490eac8673058fb514f718bb38524b957a3c5934b6749eca2ca95 in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:05 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:48:49Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:48:49Z" "architecture"="ppc64le" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:48:49Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:26:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:26:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:15 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 25 Jun 2026 23:29:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:29:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:29:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:29:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:29:13 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:15:36 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:15:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:15:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:15:36 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:15:37 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:15:55 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:15:55 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:15:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:16:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:16:03 GMT
USER gradle
# Mon, 29 Jun 2026 17:16:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:16:05 GMT
USER root
```

-	Layers:
	-	`sha256:1ce5d05f6e5641b082a71f1e9acc2940448540498097c2a35b74cf93310f5178`  
		Last Modified: Thu, 25 Jun 2026 12:13:27 GMT  
		Size: 45.1 MB (45075525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454ffa9ad55609063881c74aef17705d7d65e97d1f5ceadb3fe8c414ff22b193`  
		Last Modified: Thu, 25 Jun 2026 23:26:50 GMT  
		Size: 30.1 MB (30082746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e5d149cc004e4033be07090cd8e331ddf6ed020509a423eba34d7f6347aba`  
		Last Modified: Thu, 25 Jun 2026 23:29:53 GMT  
		Size: 158.3 MB (158348510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f107aecb1f3887d0da9c16699259ce51448035293700859c1b6c35759b7356f3`  
		Last Modified: Thu, 25 Jun 2026 23:29:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5b69b1418de1c837b20503ad54348ef67cfe5e6ecc0d2df125d1716822e279`  
		Last Modified: Thu, 25 Jun 2026 23:29:50 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e73b068a4b5ed0eae47bfbd67f30e3908e816b3c876370ef73ab68ee0f0bd8`  
		Last Modified: Mon, 29 Jun 2026 17:16:41 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61af7551e5204ada1bb4b0c50ca5b564cd92a7e991b84b510f4fb9d43f0a7d`  
		Last Modified: Mon, 29 Jun 2026 17:16:43 GMT  
		Size: 39.2 MB (39200606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fdc8cebab57bb8fd53bc282c40cefa5801d431b5d35f782b745299e475a5dc`  
		Last Modified: Mon, 29 Jun 2026 17:16:46 GMT  
		Size: 140.6 MB (140596028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8a961905604bc388414c08a556c73387d6857d29f79535e1ce3ab57f8df621`  
		Last Modified: Mon, 29 Jun 2026 17:16:41 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:57d8661dee05197067d9636208ca3d6553df7f88820e2620c6cfa4d9b7225627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0868c6d3d884531351b3b67b74f241a51acd1d28620d92349cf810f609cce57`

```dockerfile
```

-	Layers:
	-	`sha256:7bb85cfe70e28cfc524fd65fdb37d20350a502172745215974b309902ab5e5a2`  
		Last Modified: Mon, 29 Jun 2026 17:16:41 GMT  
		Size: 5.4 MB (5430693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5728c0d81a6e85ad6f59efd87af3c0a108333ecafe4cc127f89dd3b7ae7a4b19`  
		Last Modified: Mon, 29 Jun 2026 17:16:41 GMT  
		Size: 23.6 KB (23584 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:7eebf154a153f987469b788421e3df4c93491d8ae6951f14c439b5d665760a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391934593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f72f73a3055e4ff0e48c10ff2c4af20c6caa84da4a76e1aaf18a0e8d96d3a34`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:52:27 GMT
ENV container oci
# Thu, 25 Jun 2026 05:52:27 GMT
COPY dir:1e4f533284314158fe9071edbf6e5a91d133d00a252b00de728bc4926b26b337 in /      
# Thu, 25 Jun 2026 05:52:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:52:27 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:52:27 GMT
COPY dir:5b21c0bd8fdb721477bc5c6da5a748382232df7791527a89e418bc39ef6e03ed in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:52:28 GMT
COPY dir:5b21c0bd8fdb721477bc5c6da5a748382232df7791527a89e418bc39ef6e03ed in /root/buildinfo/      
# Thu, 25 Jun 2026 05:52:28 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:51:47Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:51:47Z" "architecture"="s390x" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:51:47Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:24:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:24:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:24:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:24:56 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:24:56 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 25 Jun 2026 23:26:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:26:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:26:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:26:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:20 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:11:00 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:00 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:00 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:09 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:09 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:11:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:11:14 GMT
USER gradle
# Mon, 29 Jun 2026 17:11:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:11:14 GMT
USER root
```

-	Layers:
	-	`sha256:601b4838142f06d7d4e767a327592a762187b9af6287ad5286218612b47da08f`  
		Last Modified: Thu, 25 Jun 2026 12:13:18 GMT  
		Size: 38.7 MB (38740623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13318bf4eac76cd98e559c9948f545e02787bc71d84cc1c6e26cac00f3ccd433`  
		Last Modified: Thu, 25 Jun 2026 23:25:34 GMT  
		Size: 27.7 MB (27684193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465cee39fccf026628b12b45eb844d6b50074b4391d54294aa3d2610df17eb85`  
		Last Modified: Thu, 25 Jun 2026 23:26:45 GMT  
		Size: 147.4 MB (147390163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dc477175ec7bf6ba9ec8fa70e267598b811d8093cd06d8af3d08f925e90339`  
		Last Modified: Thu, 25 Jun 2026 23:26:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b172acd639d78d160e995ae721b08eb90691a884b704bd4f79bb9322669a5c7b`  
		Last Modified: Thu, 25 Jun 2026 23:26:42 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2ce97c074939fe977ce90d4b2561dd502eaea3899d9cf66e21f9c0a67d9a28`  
		Last Modified: Mon, 29 Jun 2026 17:11:39 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fc3c65b069eac7a84717050abcd62876bc8ee25c8d2c9c31f27f7804f1223f`  
		Last Modified: Mon, 29 Jun 2026 17:11:40 GMT  
		Size: 37.5 MB (37519046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b268be4c5679e936ab52bd2e712f14174cae89ecf7300d56ddb27bac99639838`  
		Last Modified: Mon, 29 Jun 2026 17:11:43 GMT  
		Size: 140.6 MB (140596026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b9f0a0e89c9053f6ff7def384c283f012f7b43d084aa411094dd7669103c0f`  
		Last Modified: Mon, 29 Jun 2026 17:11:39 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:e47edc17f79d6f497f2d042301c7da10698a911947705e5281e8503d833bb2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d7baafea2b34af62c10d62123a84478c2b925184fd7f30f5ddcf0c32b43a80`

```dockerfile
```

-	Layers:
	-	`sha256:04518272f1fa6d651fb3ba2564c6c16aa3468aaa629413b18d4f30dbf51c68df`  
		Last Modified: Mon, 29 Jun 2026 17:11:39 GMT  
		Size: 5.4 MB (5419943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382e52140a4f5f979f0298d335097c40c3484626a9f05fec781e06afa53bbfe9`  
		Last Modified: Mon, 29 Jun 2026 17:11:39 GMT  
		Size: 23.5 KB (23528 bytes)  
		MIME: application/vnd.in-toto+json
