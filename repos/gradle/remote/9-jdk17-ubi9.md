## `gradle:9-jdk17-ubi9`

```console
$ docker pull gradle@sha256:a3ffc25da0a377303f61715d86293f91552a17e5afb01cfb29c690ef40ab07a0
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

### `gradle:9-jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:4942fc0f89eeb0f20053a25d485b5aa28a9a984c3724ec993b35dca1f81f58b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.4 MB (392442209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3694be3b36406b9925e8656bc960e72ad2ab38fd416f0404debc92ecc83e0b38`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:14:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:20 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 15 Jun 2026 23:14:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:14:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:14:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:14:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:14:28 GMT
CMD ["jshell"]
# Mon, 15 Jun 2026 23:33:03 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:33:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:33:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:33:03 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:33:03 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:33:06 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:33:06 GMT
ENV GRADLE_VERSION=9.5.1
# Mon, 15 Jun 2026 23:33:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Mon, 15 Jun 2026 23:33:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:33:09 GMT
USER gradle
# Mon, 15 Jun 2026 23:33:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 15 Jun 2026 23:33:10 GMT
USER root
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903540fee651390634086be74a3a875cedc7f7db5dac59af14e1758b8c703eaa`  
		Last Modified: Mon, 15 Jun 2026 23:14:44 GMT  
		Size: 27.7 MB (27664261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02e4505718d284f2c28a96edeb97331a0c70750f6b39105a7120ac6d9561a3c`  
		Last Modified: Mon, 15 Jun 2026 23:14:47 GMT  
		Size: 145.9 MB (145915402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bbb318d35641163243412d38d25e264f65c91f84e281df148ebdeaf411760e`  
		Last Modified: Mon, 15 Jun 2026 23:14:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aed6464a03355515f0f61d35644532e19d4ed35e0372320a05cbf8469909bb`  
		Last Modified: Mon, 15 Jun 2026 23:14:43 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7bc5869cf433a49ca1e0458c43da6fa8478e4f9b3e511de3b726a894b7e044`  
		Last Modified: Mon, 15 Jun 2026 23:33:26 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede9cf81361f0954f3cd1c671d629317a33cbb6c53d2b86483bf39962ed7cc73`  
		Last Modified: Mon, 15 Jun 2026 23:33:28 GMT  
		Size: 37.9 MB (37915592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5c653e8d802670583848b86d08b4646a690c1afaebee3e9e0d9195c9a08ec5`  
		Last Modified: Mon, 15 Jun 2026 23:33:31 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf01c756b445e4186f8b9668b228d5369194871106d77ebfbbe4c6b3ee58e`  
		Last Modified: Mon, 15 Jun 2026 23:33:27 GMT  
		Size: 25.6 KB (25620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:a3e7b725deafdc137ed6fe96b9ad59966ea0c4e70d0efe9b29dd1b7d2bcc55dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ef287589d5ea742d82eb6fb137166fe5c19556c5c59dfdc32010abfd671a1c`

```dockerfile
```

-	Layers:
	-	`sha256:fc76138dac446a937138d3e332f4414a4e7398032ecedb9ff4a0cfd1db13e5a0`  
		Last Modified: Mon, 15 Jun 2026 23:33:27 GMT  
		Size: 5.4 MB (5421112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b533059260104cc2ef9138ce8a0277111b426194358285c5ddc1f611220379dc`  
		Last Modified: Mon, 15 Jun 2026 23:33:27 GMT  
		Size: 23.2 KB (23236 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:aa1b855e9161152c68bc7de9271ac0c5326dc4a72541e193770d4703806175df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389183801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44f43ec90febe3691ac049aed03871fde42a13358981acbdea9d3cc5502b51d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:13:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:33 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 15 Jun 2026 23:13:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:13:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:13:41 GMT
CMD ["jshell"]
# Mon, 15 Jun 2026 23:25:24 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:25:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:25:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:25:24 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:25:24 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:25:28 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:25:28 GMT
ENV GRADLE_VERSION=9.5.1
# Mon, 15 Jun 2026 23:25:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Mon, 15 Jun 2026 23:25:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:25:31 GMT
USER gradle
# Mon, 15 Jun 2026 23:25:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 15 Jun 2026 23:25:32 GMT
USER root
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096de0b5e8c9d1edb60fa0b1fad281d17b7e41acd75f4dd99db0560fa0f3b71`  
		Last Modified: Mon, 15 Jun 2026 23:13:59 GMT  
		Size: 28.1 MB (28098934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435ddd9fc8136de3b72d083246bee7672dd201711201e9dc439ef53b1cff762f`  
		Last Modified: Mon, 15 Jun 2026 23:14:02 GMT  
		Size: 144.7 MB (144734844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fb66438eddb81ad0391c4ac0094648601d62a16f339f9f4036a63bc6ed0e23`  
		Last Modified: Mon, 15 Jun 2026 23:13:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e191c64bbe8b20c98dbf98001ce83f58a7a3bd8045cdf0a778d2791a7ee1a0`  
		Last Modified: Mon, 15 Jun 2026 23:13:58 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cab1d9855b850f8f7f9530f535ed7fc3eb47e694b8cf5eaf79954074f724f63`  
		Last Modified: Mon, 15 Jun 2026 23:25:49 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b764aca5ef229aa13c7840b78f28af8ad03f2f9d2090d9075bd33b3107053e6`  
		Last Modified: Mon, 15 Jun 2026 23:25:51 GMT  
		Size: 37.2 MB (37206549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be87d78a3d641b5e864b8b7bfdd359bc077300757a981a0680371f9755732a02`  
		Last Modified: Mon, 15 Jun 2026 23:25:53 GMT  
		Size: 140.2 MB (140236951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be02f0236d3de8fc31cc7e91c9832a8de20e900000bf3a28b0f20a5cdea964a`  
		Last Modified: Mon, 15 Jun 2026 23:25:49 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:8c95049193ae18a87d1f1b302ee570ef8cb182aca62f14e166e6930e55afadcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea2c0aaf02033452c2393bd5950fbbd747f0542852ad984b964f3dac1e379e1`

```dockerfile
```

-	Layers:
	-	`sha256:f5e6815cceea51b9b18a26e65a08a4e27c6f7d237a9ff1b6458e3b07cce383f9`  
		Last Modified: Mon, 15 Jun 2026 23:25:49 GMT  
		Size: 5.4 MB (5420494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1260364c9633d547a01d92a40369edd0b1ce3bc55e70987757ccff62c4b7301c`  
		Last Modified: Mon, 15 Jun 2026 23:25:49 GMT  
		Size: 23.4 KB (23385 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:911844208ae04a1a275d8abf68f37b53cbaf230e4e58c7cce548ccdc11800f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400470293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa4f7b1ee490002c5679aa3c539f89e3527bd2101abf9229f7c7f25081e5a22`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:54 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:54 GMT
COPY dir:efdade3e0178260d1a2da6ad5ac90643bb0c91f0b6715fd2f4ca2979fd79cbad in /      
# Mon, 15 Jun 2026 04:14:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:e844bf29c6ce679ad36ca75749d6db974a3ec704b6b681dbf49d34fbc703890c in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:e844bf29c6ce679ad36ca75749d6db974a3ec704b6b681dbf49d34fbc703890c in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:55 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:43Z" "org.opencontainers.image.created"="2026-06-15T04:14:43Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:43Z
# Mon, 15 Jun 2026 23:14:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:14:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:14:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:12 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 15 Jun 2026 23:19:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:19:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:19:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:19:06 GMT
CMD ["jshell"]
# Tue, 16 Jun 2026 00:03:11 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 00:03:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 00:03:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 00:03:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 00:03:11 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 00:03:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 16 Jun 2026 00:03:25 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 00:03:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 00:03:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 00:03:29 GMT
USER gradle
# Tue, 16 Jun 2026 00:03:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 00:03:31 GMT
USER root
```

-	Layers:
	-	`sha256:fd098750da592cfacf74625936c645114bdb046870485748bf918ed2db1df267`  
		Last Modified: Mon, 15 Jun 2026 06:12:54 GMT  
		Size: 45.2 MB (45156026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fbe8029dfe532f57a1538c32f741d22163601d4b4fa9e2e8a0e9afe095270`  
		Last Modified: Mon, 15 Jun 2026 23:14:51 GMT  
		Size: 30.1 MB (30096922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589a0d789ae1f9c4c7ac9230513fa17da97b6d8a9f0f3f250ccf2dd858552776`  
		Last Modified: Mon, 15 Jun 2026 23:19:41 GMT  
		Size: 145.8 MB (145788660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c7928ea1b6ab9876b0cb0a8ca28a2d9688dd47bbc96e71d8c45809e4e4db25`  
		Last Modified: Mon, 15 Jun 2026 23:19:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c47a01eb2b8fb3cd8c6bf75017ea0cb8095e14738eacbe3a873b066944ece61`  
		Last Modified: Mon, 15 Jun 2026 23:19:37 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2346eb0901fb4e8ef5489f2e4ca06e7ae5fb9b914405da70031e5bc197af8d`  
		Last Modified: Tue, 16 Jun 2026 00:04:05 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6be2d1c487a1b1012df2f566f6ea966c1cbdc0ba911910a4d9379550c032a5`  
		Last Modified: Tue, 16 Jun 2026 00:04:07 GMT  
		Size: 39.2 MB (39187151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ddf1eb968916abc254ea0022c38d7f331e02ef251435931b82036aff4347b5`  
		Last Modified: Tue, 16 Jun 2026 00:04:10 GMT  
		Size: 140.2 MB (140236992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5d65b93976c44066e7a0e5950233bb37ecac633f57436d6199ae386c7d2ca2`  
		Last Modified: Tue, 16 Jun 2026 00:04:05 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:032c513d3e5fd4b61c036b441d2307d6df382d04ad04d26857d4452508308824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752cf3ed8b29423fd2743a99c00489f1c9d8fb19e8e124e26f2f5bd2b93d589b`

```dockerfile
```

-	Layers:
	-	`sha256:257eaa66d912132af25b950f95c1b02f681cd9feeda7a0b5a6890a31620624e3`  
		Last Modified: Tue, 16 Jun 2026 00:04:05 GMT  
		Size: 5.4 MB (5418461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34847a53419f7df5a72fa4c376ab73f4d0b74667888869c15f546fae2afa990c`  
		Last Modified: Tue, 16 Jun 2026 00:04:05 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:900530b484f4180d95ba0c48025f725f794e5ff9fe525df6625314ffd401079f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380174978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14987c5d911f237cd5020a950b4845b9b2d3353ad05271a2cb0ee414246425c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:18:01 GMT
ENV container oci
# Mon, 15 Jun 2026 04:18:01 GMT
COPY dir:b287442ff3a1305f30c768257fb405a05247fad637bf642752f1eb5c150e583c in /      
# Mon, 15 Jun 2026 04:18:01 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:18:01 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:18:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:18:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:18:02 GMT
COPY file:8c615175ae26448d1bab1087e5b4f0afb27d6d1d3930dbd033fa26b49547a2f9 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:18:02 GMT
COPY file:8c615175ae26448d1bab1087e5b4f0afb27d6d1d3930dbd033fa26b49547a2f9 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:18:02 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:17:50Z" "org.opencontainers.image.created"="2026-06-15T04:17:50Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:17:50Z
# Mon, 15 Jun 2026 23:12:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:12:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:12:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:12:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:12:42 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 15 Jun 2026 23:13:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:13:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:13:42 GMT
CMD ["jshell"]
# Mon, 15 Jun 2026 23:25:15 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:25:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:25:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:25:15 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:25:16 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:25:21 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:25:21 GMT
ENV GRADLE_VERSION=9.5.1
# Mon, 15 Jun 2026 23:25:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Mon, 15 Jun 2026 23:25:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:25:26 GMT
USER gradle
# Mon, 15 Jun 2026 23:25:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 15 Jun 2026 23:25:26 GMT
USER root
```

-	Layers:
	-	`sha256:99902732bbc0758252faa428c8bd627fb473cdca6d03f791fd4b177c4a5de314`  
		Last Modified: Mon, 15 Jun 2026 06:12:36 GMT  
		Size: 38.8 MB (38806856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d124567964b233fa0f2f2c3220acab3cf5090a6eea57d13aaa5d82fbbe0c8ce3`  
		Last Modified: Mon, 15 Jun 2026 23:13:09 GMT  
		Size: 27.7 MB (27692083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860000e0f5a8a83b8f348f9b1a88ba29d16f1582db9e3c79c9069995435870e3`  
		Last Modified: Mon, 15 Jun 2026 23:14:11 GMT  
		Size: 135.9 MB (135912327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d473ba1cb3e0f2fb241635df98f1f9fdf255cfe3af5b496ca8ee9dd6d4a3aa`  
		Last Modified: Mon, 15 Jun 2026 23:14:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b694a6bb45397bbdcb4aa73cfb41b5617dcc52e5ede7c1d224ec2561a55d263e`  
		Last Modified: Mon, 15 Jun 2026 23:14:08 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59df478db8d7bda23259d1152d6f9caf935e8e041ebd50ef7f5930d9725143e9`  
		Last Modified: Mon, 15 Jun 2026 23:25:56 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5df6260bc20c15720d96a279f3efa9a9b8d4c46f14c8d36cc30fbff95f720e`  
		Last Modified: Mon, 15 Jun 2026 23:25:57 GMT  
		Size: 37.5 MB (37522189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc5464b69f901a247b472a1d21d29701ae9e3936260dbc8c6cadb098eb45917`  
		Last Modified: Mon, 15 Jun 2026 23:25:59 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069e6d84d31faec5506a196b8537ccea5f44b928ec1911bee2133cbd9519e187`  
		Last Modified: Mon, 15 Jun 2026 23:25:56 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:89c26deecf5b08494bf62e21fdbe41004e2a5cf9e5836724f554bbbd590e788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4889d29eeebaf942a140385cc85cb5a99fee9eef6e652ed23e875b254109cdeb`

```dockerfile
```

-	Layers:
	-	`sha256:9aab3214fdffad30a697a38b04e03778131c2b44407811271a4c2fab2b94fdfc`  
		Last Modified: Mon, 15 Jun 2026 23:25:56 GMT  
		Size: 5.4 MB (5407717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0114c9bf874ff44c272d796a0a99a8f6bb30dbc4c817aab80144cf92e91e1249`  
		Last Modified: Mon, 15 Jun 2026 23:25:56 GMT  
		Size: 23.2 KB (23234 bytes)  
		MIME: application/vnd.in-toto+json
