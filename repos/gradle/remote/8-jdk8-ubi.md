## `gradle:8-jdk8-ubi`

```console
$ docker pull gradle@sha256:7e6abe13addd5fd690acef09e88fbd42ff00a6cfc0dbb4fdbc9d300fa6053cbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:8-jdk8-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:98482a713df156b51b98fe1e313185501a56606fda8179be22d425b0eea091f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299294853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefdd512677f59e759a794f47a66344d3f3245bb6091c125f0173f2a3194d34b`
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
# Thu, 04 Dec 2025 19:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:24 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 04 Dec 2025 19:45:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 04 Dec 2025 19:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 20:03:21 GMT
CMD ["gradle"]
# Thu, 04 Dec 2025 20:03:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 04 Dec 2025 20:03:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 04 Dec 2025 20:03:21 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 04 Dec 2025 20:03:21 GMT
WORKDIR /home/gradle
# Thu, 04 Dec 2025 20:03:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 04 Dec 2025 20:03:25 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 04 Dec 2025 20:03:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 04 Dec 2025 20:03:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 04 Dec 2025 20:03:28 GMT
USER gradle
# Thu, 04 Dec 2025 20:03:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 04 Dec 2025 20:03:28 GMT
USER root
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58683a05ac4545db26cedb6bf069ef78065981b9418ff344b989e5547ce25b5f`  
		Last Modified: Thu, 04 Dec 2025 19:45:59 GMT  
		Size: 30.4 MB (30411196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fd6d63ce446b3c72b69a2d8e22c1e1bce85e80babbd581ae17c28aedfad9f2`  
		Last Modified: Thu, 04 Dec 2025 19:46:03 GMT  
		Size: 54.7 MB (54733890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943d48f1e0be13aedef8fdbef1876c347e0c22eb32b7eadbaa2c8b8392f12f21`  
		Last Modified: Thu, 04 Dec 2025 19:45:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce20366d02268265499b9b612d24e92c58a8fc5b442d8e08eff2351977659e7`  
		Last Modified: Thu, 04 Dec 2025 19:45:57 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d26c6d668bc3ec300bb51a1d2f429f6993aa4df0d79b19017f0bc243c36be`  
		Last Modified: Thu, 04 Dec 2025 20:03:56 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505f09bcf1936141ffd85894298ab9ac9b33df63f61b306a6ef2bc93a6c72a1e`  
		Last Modified: Thu, 04 Dec 2025 20:04:00 GMT  
		Size: 36.7 MB (36654725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939875e1bf9f746d9431d3d87a848687fced4288ea4766c55016381ff536e7d9`  
		Last Modified: Fri, 05 Dec 2025 11:07:37 GMT  
		Size: 137.4 MB (137395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a130262a90266f728068e6c2dfdae9d47f3203fef3aac70c9030317a7daed7a4`  
		Last Modified: Thu, 04 Dec 2025 20:03:56 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:7bc059825fdf4039e9231f79447469109b55add1e12dd9e81d64674b4d4c8970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b01c9891f190854e37c2dfc4741bc7a5516c3889ccbd06a38e71a5e75b06b4b`

```dockerfile
```

-	Layers:
	-	`sha256:1687c4f75b1458eb57b3c1b563c0a4605f41e512ab6dd8488841067f49e82cc0`  
		Last Modified: Thu, 04 Dec 2025 21:22:13 GMT  
		Size: 5.5 MB (5524759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:240a553d24f4dcfb474edf02654a07f3ca2774f52264fe395f3d90fffe9af3d8`  
		Last Modified: Thu, 04 Dec 2025 21:22:14 GMT  
		Size: 24.2 KB (24170 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2071a08feb30964c9f5c94bb6d84fa51986910ad86b0bf4232640b036cbadf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296404050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cc0092ed8087dcbe2cd6b9e7773a69776edcbbd80737b375b8fb00083946b9`
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
# Thu, 04 Dec 2025 19:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:34 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 04 Dec 2025 19:45:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 04 Dec 2025 19:45:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:45:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:45:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 20:04:28 GMT
CMD ["gradle"]
# Thu, 04 Dec 2025 20:04:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 04 Dec 2025 20:04:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 04 Dec 2025 20:04:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 04 Dec 2025 20:04:28 GMT
WORKDIR /home/gradle
# Thu, 04 Dec 2025 20:04:32 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 04 Dec 2025 20:04:32 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 04 Dec 2025 20:04:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 04 Dec 2025 20:04:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 04 Dec 2025 20:04:34 GMT
USER gradle
# Thu, 04 Dec 2025 20:04:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 04 Dec 2025 20:04:35 GMT
USER root
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec676fe798b3fc0426feeeb4fb25b636d3dedf7cff93007f9e1941bf91249f`  
		Last Modified: Thu, 04 Dec 2025 19:46:38 GMT  
		Size: 30.9 MB (30855171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cc521c9d0c4db0b965c0dc7b34a658f37301b6ce847f2ae95063a7f997e713`  
		Last Modified: Thu, 04 Dec 2025 19:46:22 GMT  
		Size: 53.8 MB (53815554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde8ef87532b408fc2bd228eaea1434c41a54fc8e6dea7dbadff9028ebc09446`  
		Last Modified: Thu, 04 Dec 2025 19:46:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1ff55a59dcacbb0924c7635bb363ee443cbb8e28653d25187b189397b6836`  
		Last Modified: Thu, 04 Dec 2025 19:46:12 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebc1f0b1d6f040db2dab57fba33be6be9833ee6c3bdc2e8239ba4cc164ac161`  
		Last Modified: Thu, 04 Dec 2025 20:05:01 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc8f56e943528e9631e323db6586413ba6e6114aab2cc10c8532e44705c2bd2`  
		Last Modified: Thu, 04 Dec 2025 20:05:11 GMT  
		Size: 36.1 MB (36051571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc856aef0f79541ff8fc1c390d612dbaf14f138d3dee54d322f973ab04d81ba0`  
		Last Modified: Fri, 05 Dec 2025 00:57:30 GMT  
		Size: 137.4 MB (137395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed142a43461649a229e7e282c38c455a9502d9e83d2e8dbea629b0e4bcd81455`  
		Last Modified: Thu, 04 Dec 2025 20:05:01 GMT  
		Size: 59.5 KB (59549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:f5a8bf86584b2d86276d3c3e3affb9a4f2b5be21df33191a620df09ee78b779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5549253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171b5ea74c61657437c43436dbd856e11284059647772e88cae3dfede05084aa`

```dockerfile
```

-	Layers:
	-	`sha256:37bc89e0e4375634c65b660650041a31add72fe7bb7f72e34ef0b58c1cbf5539`  
		Last Modified: Thu, 04 Dec 2025 21:22:19 GMT  
		Size: 5.5 MB (5524887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9840ddbf36c0c6e8837dc99be8facb42540c749314ca86c0040e07e14317beae`  
		Last Modified: Thu, 04 Dec 2025 21:22:20 GMT  
		Size: 24.4 KB (24366 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:59912379566e7086baa376ece1157b7abbf3d29b571b7998ba02613559e125bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304825603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e3976474613d19e919a175b0030b827ee7a1eb2cbb61a9b742ad231827cf0c`
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
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 04 Dec 2025 19:46:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 04 Dec 2025 19:46:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:46:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:46:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 20:10:44 GMT
CMD ["gradle"]
# Thu, 04 Dec 2025 20:10:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 04 Dec 2025 20:10:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 04 Dec 2025 20:10:44 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 04 Dec 2025 20:10:45 GMT
WORKDIR /home/gradle
# Thu, 04 Dec 2025 20:11:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 04 Dec 2025 20:11:05 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 04 Dec 2025 20:11:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 04 Dec 2025 20:11:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 04 Dec 2025 20:11:11 GMT
USER gradle
# Thu, 04 Dec 2025 20:11:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 04 Dec 2025 20:11:13 GMT
USER root
```

-	Layers:
	-	`sha256:0dbaabed7cc8118dfa57a21ab03f83f55ba784110782e2081afc710ef3eb3c16`  
		Last Modified: Thu, 04 Dec 2025 00:10:07 GMT  
		Size: 44.4 MB (44445850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbc041c92aa38c134e96bedbac7c177760045bc5616488fd3fda3e26cca1a60`  
		Last Modified: Thu, 04 Dec 2025 19:46:52 GMT  
		Size: 32.9 MB (32890492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5be981d78ff474337627c1818baada0068c41f6d548ca2498e2a5ae34de807f`  
		Last Modified: Thu, 04 Dec 2025 19:46:58 GMT  
		Size: 52.2 MB (52175843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913ac54b70e89f669c894f683f01eda37a6620d448aef1f81377704dfe8b5`  
		Last Modified: Thu, 04 Dec 2025 19:46:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24c161862c2a4a0cd62cd5dc5e55f2587ee36d66ccf679bcd929fb5e910b68`  
		Last Modified: Thu, 04 Dec 2025 19:46:49 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88009bd22eb9db46b7c23909c617af363188bb2b1e2ae15f4297728cc01214cd`  
		Last Modified: Thu, 04 Dec 2025 20:12:04 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb64a3d5b2224973fe13ddcb97f7305830ab6754e96bd2dd8e1fbd42cbf0802`  
		Last Modified: Thu, 04 Dec 2025 20:12:21 GMT  
		Size: 37.9 MB (37879030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21efae3b981348f28603d8b9a87c76f788cfdcf481ed9f94f1cf5c2e8ea12672`  
		Last Modified: Fri, 05 Dec 2025 19:20:07 GMT  
		Size: 137.4 MB (137395197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3401caa310ec4176f8bc6417f2d0141a64167c0cd65c7ac20ab0e85e71db7`  
		Last Modified: Thu, 04 Dec 2025 20:12:04 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:38250e1df267f2b66143da0d981a0efa5827bf4ee91eb82ab863781f93d40d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fae06b88148e4ac03fbcffe8696daa4c54d7f7f737daa72426a37f97f5c2bc`

```dockerfile
```

-	Layers:
	-	`sha256:e382751c11a3284157dba765862464e353c61a3629162e03135ca7d8219cfcaa`  
		Last Modified: Thu, 04 Dec 2025 21:22:25 GMT  
		Size: 5.5 MB (5522687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb4cbfd2a2ecc48f102be9f47d04856c62e8c6b6603c5fd113727c89aa79ce3`  
		Last Modified: Thu, 04 Dec 2025 21:22:26 GMT  
		Size: 24.2 KB (24243 bytes)  
		MIME: application/vnd.in-toto+json
