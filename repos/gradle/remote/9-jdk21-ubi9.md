## `gradle:9-jdk21-ubi9`

```console
$ docker pull gradle@sha256:6b3746e21d462e5320e1afda44cb282b1e077b8397518354fe6f6e027907e2c4
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

### `gradle:9-jdk21-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:ae4e80127c235c0fb0dd0b43b2ed77e1c01d167a7539c7c68c756ebf00c896e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402542040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42a1d07a60a99796132efdfeed6fc5d781c8f1bf5800c9139191c4a4d674453`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:47:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:47:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:47:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:47:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:47:15 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 04 Dec 2025 19:47:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 04 Dec 2025 19:47:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:47:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:23 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:44:56 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:44:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:44:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:44:56 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:44:56 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:45:00 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:45:00 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:45:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:45:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:45:02 GMT
USER gradle
# Fri, 16 Jan 2026 21:45:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:45:03 GMT
USER root
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1380ed9b5f046f3e19daab30c700d932ad89db8a37144dfc1f59a118759e66d`  
		Last Modified: Thu, 04 Dec 2025 19:47:41 GMT  
		Size: 30.4 MB (30411178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ef207506a6bb01a16d70e58b97f98a85a65b64c44164d7ed050697a838a9e`  
		Last Modified: Thu, 04 Dec 2025 20:01:34 GMT  
		Size: 157.8 MB (157828921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d124e40e074dac339f2255149ce6def8396194a84dccd3408a058b82d31963ce`  
		Last Modified: Thu, 04 Dec 2025 19:47:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b33abbc635e31b95c70220e420935dfe8cbfa0df3bd3d182ad3ce9ab6bdfa0`  
		Last Modified: Thu, 04 Dec 2025 19:47:50 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25336498009e993c5c8e66ecc940598d732e5061c3dbbbc30408ee11bfac90d`  
		Last Modified: Fri, 16 Jan 2026 21:45:27 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb364a0be5c6cd05dfadf17bd16f53d51f0c5ea43fd627846bfae293c5a7352`  
		Last Modified: Fri, 16 Jan 2026 21:45:44 GMT  
		Size: 37.2 MB (37242544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac39d5c1c285a3a94d9a72f92e7fdc3b8645d501dac8562f9d5dd77e961c7283`  
		Last Modified: Fri, 16 Jan 2026 21:45:22 GMT  
		Size: 137.0 MB (136988877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14257be86d4ab273bc775f547607494c85a6f257d16607bda3d4d337059ad60`  
		Last Modified: Fri, 16 Jan 2026 21:45:19 GMT  
		Size: 25.6 KB (25596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:c2315bd0c854ac19b4146175cc906c20f6d8b59d5033b33a49f01d51f4d65ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0dbe80d99677ee6b905213a134983c404845d9421c593f72760180e37f660c`

```dockerfile
```

-	Layers:
	-	`sha256:0fbce39223edcb6c335ffe9ed976516d8d3aae86e368b3a6175fd8f90b24194e`  
		Last Modified: Fri, 16 Jan 2026 21:45:19 GMT  
		Size: 5.4 MB (5388539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e25501f92de4a832203390999c4a01a767c774e68bd628da6d3751ec5e8d4650`  
		Last Modified: Sat, 17 Jan 2026 00:26:24 GMT  
		Size: 23.5 KB (23490 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:28f193f7cf902e52e250f570edee14efe44c9a6f0bc5d218fd2e805d68daef5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398781115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2bfeedaaf1117283e0d2a6546a77b2d46b1a4f926584a493a8d80235d2b73c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Thu, 04 Dec 2025 19:46:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:46:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:46:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:46:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:46:21 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 04 Dec 2025 19:46:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 04 Dec 2025 19:46:30 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:46:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:46:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 19:46:30 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:45:32 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:45:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:45:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:45:32 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:45:32 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:45:40 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:45:40 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:45:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:45:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:45:43 GMT
USER gradle
# Fri, 16 Jan 2026 21:45:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:45:43 GMT
USER root
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:00:49 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83cee7c71c9193c071c958a345e3a74f08ba26ec78d7cbec425ae44c673214d`  
		Last Modified: Thu, 04 Dec 2025 19:47:04 GMT  
		Size: 30.9 MB (30855151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c57dcf2782586b67a045f8efaacbcedcb6b3c549774a76a0fa0735f22b9538`  
		Last Modified: Thu, 04 Dec 2025 19:46:52 GMT  
		Size: 156.1 MB (156111789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449530f5a8e47af3ec618bfc612adb3aa3a4a374c76d1dda83e750bc6a985ad4`  
		Last Modified: Thu, 04 Dec 2025 19:46:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecace5da008605e95edc88ead2b95e15e597ace09fee5d07b3b115394a802485`  
		Last Modified: Thu, 04 Dec 2025 19:46:57 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0af2c8a3b1ed693a019c0ceda572c9f561f86771a67b16a3dd38f3b043de3f`  
		Last Modified: Fri, 16 Jan 2026 21:46:00 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f437f7a1708da123847d2ba9732ee4602eaba20b9598febe3cfd4441ff6ead93`  
		Last Modified: Fri, 16 Jan 2026 21:46:02 GMT  
		Size: 36.6 MB (36568983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26014fef8e3bf900ca7c39a7892edc5a640f472585c18e0cb68b6054bfe97f2c`  
		Last Modified: Fri, 16 Jan 2026 21:46:04 GMT  
		Size: 137.0 MB (136988877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000cf8511c7b3e36aa496da5f6a436502eec6f5afd90d2f14f00723987429b7e`  
		Last Modified: Fri, 16 Jan 2026 21:46:09 GMT  
		Size: 29.3 KB (29321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:7110773269e12be6ad181e9d0b6754376dcfe314a6ca0784ca916c220c25a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5411584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65eec5dc3d6778ff2156db21558097d9da6e042bda16f338f8ad9f3cac7b3a3e`

```dockerfile
```

-	Layers:
	-	`sha256:0452dbb59274a64c477546d53b8acd20a4e899799e1d4a02d256f851ee741af3`  
		Last Modified: Fri, 16 Jan 2026 21:46:00 GMT  
		Size: 5.4 MB (5387933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497923cefd49b55bd392aa343a22ffdfb6967755625d6ea81d54d8457ac77524`  
		Last Modified: Sat, 17 Jan 2026 00:26:30 GMT  
		Size: 23.7 KB (23651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:d409dfdf585842c0e51802b95c6fb46f1d26a837962e9777f9ce391874b26350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410792848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a093ef8aa4ed08c650666eddf847bd17ce769262e63cce52eeebafb5839fcd2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:38:00 GMT
ENV container oci
# Wed, 03 Dec 2025 20:38:01 GMT
COPY dir:1944394b2cb85c8bd1da6ad676bb75b09725617f627438630bb53946c4695c4a in /      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:38:01 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:e9df47e0f73aa3fdb7704b0b5f90208619f4101460f662007af9ba5df5a06a9e in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:e9df47e0f73aa3fdb7704b0b5f90208619f4101460f662007af9ba5df5a06a9e in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:38:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:37:49Z" "org.opencontainers.image.created"="2025-12-03T20:37:49Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:37:49Z
# Thu, 04 Dec 2025 19:45:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:52 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 04 Dec 2025 19:50:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 04 Dec 2025 19:50:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:50:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:50:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 19:50:14 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:49:39 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:49:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:49:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:49:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:49:44 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:50:30 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:50:30 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:50:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:50:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:50:37 GMT
USER gradle
# Fri, 16 Jan 2026 21:50:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:50:38 GMT
USER root
```

-	Layers:
	-	`sha256:0dbaabed7cc8118dfa57a21ab03f83f55ba784110782e2081afc710ef3eb3c16`  
		Last Modified: Thu, 04 Dec 2025 00:10:07 GMT  
		Size: 44.4 MB (44445850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbc041c92aa38c134e96bedbac7c177760045bc5616488fd3fda3e26cca1a60`  
		Last Modified: Thu, 04 Dec 2025 19:46:38 GMT  
		Size: 32.9 MB (32890492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234486334d886ac5c9d7ae688c3d98785796109551788b4bcf8c1412ce72add4`  
		Last Modified: Thu, 04 Dec 2025 19:51:01 GMT  
		Size: 157.9 MB (157943411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1a53c1ad3da6af971514d17d87c6e3a8c9ab63e8ae78c227e464dd43a54aa0`  
		Last Modified: Thu, 04 Dec 2025 19:51:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25298c277c7fc4552993ac1aa02728d72af8ae8b0567d2663b1a0d7953c86150`  
		Last Modified: Thu, 04 Dec 2025 19:51:08 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab91f2b487e8e844fa1c9fd4fdf77d9191646b876c4203b14b352b8b18c78c6`  
		Last Modified: Fri, 16 Jan 2026 21:51:21 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0955f7fd2340ce458e4ec73a051fef1e24899bcae02705ea845482a62f0429d2`  
		Last Modified: Fri, 16 Jan 2026 21:51:36 GMT  
		Size: 38.5 MB (38519670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d989c42c8261661ba5706049329ceb6434dcf04d0cedb9eb6215586d24823a10`  
		Last Modified: Sun, 18 Jan 2026 12:11:42 GMT  
		Size: 137.0 MB (136988872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710691b9de8051231a258657cdf23a8472c283aab3cd339c5feb83cc8de7050b`  
		Last Modified: Fri, 16 Jan 2026 21:51:31 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:8d52751f6a74e9af0b5a7fd789de1f2dbbebec395b82e3218cd425f6afeeb593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5409400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004b9e211976961403e0cc3432ded436324b87bdb522e2e1adcc5a40187bfdda`

```dockerfile
```

-	Layers:
	-	`sha256:130c919c4591336e9c45bee9970832364f03452dcfb0219d7aa48edf2d61c8ff`  
		Last Modified: Sat, 17 Jan 2026 00:26:39 GMT  
		Size: 5.4 MB (5385856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2bc3fcd878df17b0e68bc94b799b4b881cf513db0272205047f99717e610b20`  
		Last Modified: Sat, 17 Jan 2026 00:26:40 GMT  
		Size: 23.5 KB (23544 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:6079f9147f45fd9ab3f37cf7e6538cb13284de9955b620e27fd463b968596390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 MB (389523940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9c4c52803cceb398262783d5f27f471ffbb4770dd56134a6f1cb80463a48d0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:42:43 GMT
ENV container oci
# Wed, 03 Dec 2025 20:42:44 GMT
COPY dir:10eb0792500239f5e33d6b6b7941aff62593a46d7fd8ece7d8112154ea3105b1 in /      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:42:44 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:f78d6df7f6c9ff8f12b4cd77c81f39d3e176ca1a669ebe7b8a04c5beb6be6145 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:f78d6df7f6c9ff8f12b4cd77c81f39d3e176ca1a669ebe7b8a04c5beb6be6145 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:42:44 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:42:32Z" "org.opencontainers.image.created"="2025-12-03T20:42:32Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:42:32Z
# Thu, 04 Dec 2025 19:45:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:27 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 04 Dec 2025 19:47:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 04 Dec 2025 19:47:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:47:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:21 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:45:08 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:45:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:45:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:45:08 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:45:08 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:45:14 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:45:14 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:45:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:45:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:45:17 GMT
USER gradle
# Fri, 16 Jan 2026 21:45:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:45:18 GMT
USER root
```

-	Layers:
	-	`sha256:8d6bf9619dce2b1902cecb7448c5bfe74272c22bbdc9eb02a2de550b72a7db66`  
		Last Modified: Thu, 04 Dec 2025 00:10:07 GMT  
		Size: 38.1 MB (38133803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32d5166444cb69244412d0ff236358d3d5c91712123606bd5849ef6a3411abf`  
		Last Modified: Thu, 04 Dec 2025 19:46:05 GMT  
		Size: 30.4 MB (30445196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23867dc34da812d616ef6f4828d65ff89cbea538fcbe3cd164f2d4133186082`  
		Last Modified: Thu, 04 Dec 2025 20:02:38 GMT  
		Size: 147.1 MB (147068498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46c836fd5b55def782c183621f21495d08db07acd3512aca56d20f5df2d8e2`  
		Last Modified: Thu, 04 Dec 2025 19:48:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc8ad9ec0808e92c23b7c726831861577366b7eb1899097320741fc079bbdbc`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb5bb7545ad63f08605c6e9e9ef320c048d896ab67c29642739194759932fd0`  
		Last Modified: Fri, 16 Jan 2026 21:45:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26ffacad18f6c1de4a5f2b8135c6053b4316392a690aefecf913ecdc7b34d61`  
		Last Modified: Fri, 16 Jan 2026 21:45:45 GMT  
		Size: 36.9 MB (36883019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf2714df26b4e33584c949ab1442185d1bf0fc2a09c7cf5b2a8d9cd0ff4bc39`  
		Last Modified: Fri, 16 Jan 2026 21:45:50 GMT  
		Size: 137.0 MB (136988880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8499c2f05bff48c15e0c92ca2ee6f97bde35dffff8865acad11c4d3250b8bb`  
		Last Modified: Fri, 16 Jan 2026 21:45:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:07e5f722a46744986b450c21aa84a5a9be10d05b3ca97acbca1b2cd40a5cb160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95fcd1d2388789c4bd3812aade60d4702b3c4f3c369d0b156a69cb573547a21`

```dockerfile
```

-	Layers:
	-	`sha256:894aecb0834de99ec39bbd98e6f7d94beccb76749640c97afcc43f5fa238d217`  
		Last Modified: Sat, 17 Jan 2026 00:26:47 GMT  
		Size: 5.4 MB (5375144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d084e41d169456c26dea48b7470293834a1b15e570e295c31bdd7cf79d608a4`  
		Last Modified: Fri, 16 Jan 2026 21:45:44 GMT  
		Size: 23.5 KB (23487 bytes)  
		MIME: application/vnd.in-toto+json
