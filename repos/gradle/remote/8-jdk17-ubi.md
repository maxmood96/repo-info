## `gradle:8-jdk17-ubi`

```console
$ docker pull gradle@sha256:27bd5f5de6654224932f011185f3ffa88bb23acb6b33011969d7b53794218914
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

### `gradle:8-jdk17-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:7408e91da768c4fc380d117f10a6cf87fca8975b744f1bca3799676cf7824808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390303021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1096e32d8122e29edfe357d3616e2587ad28ce2b5cbe836097ff4acfec8977a6`
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
# Mon, 15 Jun 2026 23:34:10 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:34:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:34:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:34:10 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:34:10 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:34:13 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:34:13 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 15 Jun 2026 23:34:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 15 Jun 2026 23:34:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:34:16 GMT
USER gradle
# Mon, 15 Jun 2026 23:34:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 15 Jun 2026 23:34:16 GMT
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
	-	`sha256:ec60c105d8e5681793a9300a77ea6a8fa5661e6769ee0c1e44840978d32faa7d`  
		Last Modified: Mon, 15 Jun 2026 23:34:31 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b95a249aab4d6c59884eaddbab4f0b73f13cd628818b975d25b226201fde88`  
		Last Modified: Mon, 15 Jun 2026 23:34:33 GMT  
		Size: 37.9 MB (37915569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca7e35fab7a9b97ae951c5149d4b1b60543edff40ce844f0dc8698f82107ba1`  
		Last Modified: Mon, 15 Jun 2026 23:34:35 GMT  
		Size: 138.1 MB (138068536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75c8ca7b184f238eb0aea42542aa805f77465de6e9961abd756b46702a528f7`  
		Last Modified: Mon, 15 Jun 2026 23:34:32 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:0844c920a201f5c448c0c8f74b3d5a41bb57ecbf8474cfdc7edb412ee44825ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c260fb490cf5a175171e7a70cc2d9c25bb51951d9830f49f7ef9ccf34802594`

```dockerfile
```

-	Layers:
	-	`sha256:6cb03783a16fa5adad418fd4d40cba3d04e14d2e0d76fe1ea6ef6a8c490cab38`  
		Last Modified: Mon, 15 Jun 2026 23:34:32 GMT  
		Size: 5.4 MB (5407054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bace9ff4075f0dd7171e7d1588ff2b4271746f1ad82088d472422d45c083a1`  
		Last Modified: Mon, 15 Jun 2026 23:34:31 GMT  
		Size: 23.8 KB (23844 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5e2fc61212c86fa190fa11074f5fd757dd8603e8fa8d96189cf355808febf3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (387045612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf04f1964a8a8e88e883634ada27f53f524eae750c7cdb07cfd2f7e94676400`
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
# Mon, 15 Jun 2026 23:26:04 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:26:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:26:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:26:04 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:26:04 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:26:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:26:08 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 15 Jun 2026 23:26:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 15 Jun 2026 23:26:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:26:10 GMT
USER gradle
# Mon, 15 Jun 2026 23:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 15 Jun 2026 23:26:11 GMT
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
	-	`sha256:04cbefb5b583cfa1ab1d7a91543f8e3f96d89cba691c12eaae13d7b8db96d5f9`  
		Last Modified: Mon, 15 Jun 2026 23:26:27 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edb1845359e9c14a9a50113c2712f5ac51158af36a0c9c1e27243c4c570492e`  
		Last Modified: Mon, 15 Jun 2026 23:26:29 GMT  
		Size: 37.2 MB (37206590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ec88a735daa80fe98e9e309550296f1640d6c81583e4e326825884522f4af1`  
		Last Modified: Mon, 15 Jun 2026 23:26:32 GMT  
		Size: 138.1 MB (138068536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1d1ae841683cf17c8185caf9c0fc0d1910537e6aab726992e07bca98845af1`  
		Last Modified: Mon, 15 Jun 2026 23:26:27 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:165293f8a436559f66f088b7cbaf8f025ab5a23dd0112ea457286280df39c8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208a59b7865bf70645109f7e807aac25c821ab042df62ea78c36c2f84e1b0765`

```dockerfile
```

-	Layers:
	-	`sha256:e0499431bf4ba362c602fbc58ab6bebe875002ad31f7afcbed8593cdca9965df`  
		Last Modified: Mon, 15 Jun 2026 23:26:28 GMT  
		Size: 5.4 MB (5406460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3014ea64ea6105ec7f2369e22a0873fa6f4aeaf6fc43db0a7d6857d6440e5456`  
		Last Modified: Mon, 15 Jun 2026 23:26:27 GMT  
		Size: 24.1 KB (24053 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:dd5efb5841913f00c6c831d45dc2d887f9ff9247a9cced5ca6abc391cbdcf2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 MB (398336471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a940795792b38369e80df8c20d74edda2cd0a0cac146e81014e717a26c1ee0d`
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
ENV GRADLE_VERSION=8.14.5
# Tue, 16 Jun 2026 00:03:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 16 Jun 2026 00:04:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 00:04:49 GMT
USER gradle
# Tue, 16 Jun 2026 00:04:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 00:04:50 GMT
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
	-	`sha256:debb014b191e384ec73c88d4cb985215cf06c2c34b0c2801e061d5f7364a8181`  
		Last Modified: Tue, 16 Jun 2026 00:05:25 GMT  
		Size: 138.1 MB (138068539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ed58a26f069b5367ca30acc105f86b7fdf9749e4486526cc5417445df17380`  
		Last Modified: Tue, 16 Jun 2026 00:05:22 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:ab9af0a997590bdbaab7bc2121804ef281750bd801f816be9e82d77abadd228d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5428357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d659330333249755022aa01dde9b1b9e7ad15c3c82bff5040672ff9df07107dd`

```dockerfile
```

-	Layers:
	-	`sha256:4e4385950940f603eef96092e16694581ab340b41bce11f5bb9acf663a3bedbc`  
		Last Modified: Tue, 16 Jun 2026 00:05:22 GMT  
		Size: 5.4 MB (5404415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2167c9592216c3294d5ce5244210adc13dc723cdf92383acec34b4e5d9b3bcca`  
		Last Modified: Tue, 16 Jun 2026 00:05:22 GMT  
		Size: 23.9 KB (23942 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:693ba157a0478da797d3cc8ff3ae8e889cb1ed004386f3a098327e0a4e37eced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.0 MB (378041167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1824cce722f20692e0c615fdf01de552f892a5c41754b38327bb063bc86e1f`
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
ENV GRADLE_VERSION=8.14.5
# Mon, 15 Jun 2026 23:25:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 15 Jun 2026 23:26:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:26:19 GMT
USER gradle
# Mon, 15 Jun 2026 23:26:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 15 Jun 2026 23:26:19 GMT
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
	-	`sha256:df1e9ef8b5d738f80395c785ebe75515fcf8bca07a1bff7a49e4c96d9dc15a6a`  
		Last Modified: Mon, 15 Jun 2026 23:26:48 GMT  
		Size: 138.1 MB (138068548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473c4ea9cd94a40c839477bb31144bc6f14b60119d9f37fe1a7179d237935e18`  
		Last Modified: Mon, 15 Jun 2026 23:26:45 GMT  
		Size: 35.0 KB (35003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:006fbd4d2022fbbd3fb427d497f62669ad749d803fbc36ebe8bd516d9c2f0643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bc368ada64a4033ac6cd3140592bdf120e91dd2139c8479d5707e0a6e76780`

```dockerfile
```

-	Layers:
	-	`sha256:2185acf9b7b9d5c55a1a62548bb9bfa0470de5cb1d9505af0140b28638243b21`  
		Last Modified: Mon, 15 Jun 2026 23:26:46 GMT  
		Size: 5.4 MB (5393659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d86fee52d5c1684e5f2f8e0ffd4240a164a82fdfc924b234afd62dae6ef33d55`  
		Last Modified: Mon, 15 Jun 2026 23:26:45 GMT  
		Size: 23.9 KB (23879 bytes)  
		MIME: application/vnd.in-toto+json
