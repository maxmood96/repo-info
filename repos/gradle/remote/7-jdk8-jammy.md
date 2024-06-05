## `gradle:7-jdk8-jammy`

```console
$ docker pull gradle@sha256:ef58865831c31a181b45e5ab27c3895a50b76ba3730075477b0032dc366e379d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:cb4a77c390440864fde19be52444f86b934100f4a6376f686652dfeb44a68368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321287530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaf1c61ce4d2a63a40a375521e451713168f3a2dc65134b65185c67e7c8d6b6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e45d0613efd61a228711b605bed73656e9264ea4e85a54c6366ac58920eaf`  
		Last Modified: Wed, 05 Jun 2024 04:58:12 GMT  
		Size: 103.6 MB (103602301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5cf131c160444e4dd84d7f506cb8d39684b08e78531d1b99246883b23750fa`  
		Last Modified: Wed, 05 Jun 2024 04:58:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe94f8a20ad35a3d79e96646cdb15f6d109646b5b133be6af32e6f32d7e6120`  
		Last Modified: Wed, 05 Jun 2024 04:58:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6d289623c1d721ffcc24fdd75d324684da528b2f981db380ce47bfb20a0c9c`  
		Last Modified: Wed, 05 Jun 2024 06:12:36 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac912f83b9e9a464eb19d632a883b17b5c2f1ac87db1df22f46f5a71016f824c`  
		Last Modified: Wed, 05 Jun 2024 06:12:37 GMT  
		Size: 51.6 MB (51550536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af192a58db5f22c7f0490a0566579d90c9102e48f018b6acbea4559f922f01f`  
		Last Modified: Wed, 05 Jun 2024 06:12:38 GMT  
		Size: 122.7 MB (122730501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294a907566bb107c3d26520fba1e525ce44f942a7e5f9126404a599018bc840d`  
		Last Modified: Wed, 05 Jun 2024 06:12:36 GMT  
		Size: 54.9 KB (54891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e616145f6e9600878811e662c4d0ec74f71c56b41fe42dc60eb03497cb064f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6989987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c253720dbfa0b706e1d496150a5748a015fffd74eff67625c5d1767e9c63d7e`

```dockerfile
```

-	Layers:
	-	`sha256:9a1ed8d0095dc7d8e9681d4512c5d42c0ede3f13a2bc2aebeffb88e15b57e4eb`  
		Last Modified: Wed, 05 Jun 2024 06:12:37 GMT  
		Size: 7.0 MB (6967781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e39a8308923787fc73b4f610f52a4583ac109a00778a5f8da09d71d40f7c27a`  
		Last Modified: Wed, 05 Jun 2024 06:12:36 GMT  
		Size: 22.2 KB (22206 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:7a72725fbbf9ca95b509bb90ced0a2a2143378ae3e9cecd6c5c0cee751b35b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.9 MB (315911622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dba676836e9a7a763d0784b9b8f58202d2fff80fc61848f0dc3c3c589f8417`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e7d8e2026f154f12e834d8b72426c2f71c8a555d373336fddba91616868b7`  
		Last Modified: Wed, 05 Jun 2024 03:59:49 GMT  
		Size: 12.5 MB (12493203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95298bffd1c0ebd593eeb6754e0f5e5ba9ca25454af388f78cd657152f59cd01`  
		Last Modified: Wed, 05 Jun 2024 03:59:55 GMT  
		Size: 99.2 MB (99228750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d783cd2973ac4c20fae7efd4d2e605cff4de71ba08f4110510a1e7d7dc0239b5`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d32d80ad9bff0aadc9f16c0712d2e20cc58ddf491fba50571fccb3d0d77f9`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83177144ef1dfad6ac5ae69007bd712d1359fdb070323036a065485b3532443a`  
		Last Modified: Wed, 05 Jun 2024 06:42:25 GMT  
		Size: 4.3 KB (4300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba2f72d093306cd13f3f5111b62c254ce616580aa9f26ebf1009712612160f6`  
		Last Modified: Wed, 05 Jun 2024 06:42:27 GMT  
		Size: 53.9 MB (53887769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697b6422ef0e661f84ec39aff4056121c0797f7364667dad9bf8869e2d599279`  
		Last Modified: Wed, 05 Jun 2024 06:51:42 GMT  
		Size: 122.7 MB (122730528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8cf493a4140336f8fd5b74219cec0c764181a4f5b3f038e5e121137c5c981c`  
		Last Modified: Wed, 05 Jun 2024 06:51:39 GMT  
		Size: 31.3 KB (31291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:d1a71602d3fb82e4b3dfcdb78514a7273c7c362f4dddafe5f685497cbf6d7fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6992025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0890f76e6fe7cab0603a3468f81561a7d12399e0372ae938a34a6ab31de057c6`

```dockerfile
```

-	Layers:
	-	`sha256:4503b183990a5330533012a342452df88d0e899a7961b891dd3ea9d9bdb36842`  
		Last Modified: Wed, 05 Jun 2024 06:51:39 GMT  
		Size: 7.0 MB (6969700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e440731f7c365dcb32f241a513de562cc2c61a549e7353e1da5efd48d859b9cc`  
		Last Modified: Wed, 05 Jun 2024 06:51:38 GMT  
		Size: 22.3 KB (22325 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:195dd1fd798e61bd0a8567c92560be0d8a8c2b7bd849c0862c315667df2f432a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.9 MB (317859949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf7ed6a13725f571b96cd523b8252cea15c2389e4f2f2c96f6a6d3aa07a2b0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2472ac6840da0115175cae8b0be8d1b8c2b6b74acb5fc6bf185b0c9333b8a3`  
		Last Modified: Thu, 02 May 2024 04:17:28 GMT  
		Size: 12.8 MB (12847034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c050069391baee7bb13200b3297c944c954a22f0428769272d51e6cba8118a36`  
		Last Modified: Thu, 02 May 2024 04:17:34 GMT  
		Size: 102.7 MB (102704159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd259c2f39c587be8bdd17660976c6158388173b58e226f2b5095d399cf658f2`  
		Last Modified: Thu, 02 May 2024 04:17:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22bcaede3cb82201c2804d7a050cbf18f994bd6f0b34f3ec133a47cc3c24ca9`  
		Last Modified: Thu, 02 May 2024 04:17:27 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639e31e6df0b38887d3cbb36f2df5b913034371be3c34c85af1e5d83d2a602a6`  
		Last Modified: Thu, 16 May 2024 22:28:17 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab98923b1fb265be1f2f3b6119f8743cb9d0d5aee16fe56c1a7261f2e7bca7e`  
		Last Modified: Thu, 16 May 2024 22:28:20 GMT  
		Size: 51.1 MB (51112273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a45f3ee0481f8d16d79b257b234ace1747c854f86629783a0ba12c9096152d3`  
		Last Modified: Thu, 16 May 2024 22:42:46 GMT  
		Size: 122.7 MB (122730533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840cbcffeec82f989c7ac493a34456a850f40dff3dc91ebd5946e615997a62be`  
		Last Modified: Thu, 16 May 2024 22:42:42 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e1fdbcfc975986a187e8713fe960627b7b128ef1c0cb12f505be2b4496779d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6996407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad23e9c5c2019996a2de1cdf404cbb8a6b0cc0182a3f8d0f14a6e9709dde9f3`

```dockerfile
```

-	Layers:
	-	`sha256:6d75add4017b81c0167fb0dcdfcac846fe9bb656734d70fa06f467bcf3b99192`  
		Last Modified: Thu, 16 May 2024 22:42:42 GMT  
		Size: 7.0 MB (6974187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8073ecfc4b848ecdb75494e76affcbb71e178bda81d52aa535f2048462f856a3`  
		Last Modified: Thu, 16 May 2024 22:42:42 GMT  
		Size: 22.2 KB (22220 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:0c04e6609d0b93b357e29d7ba3a32980de5697d87b2c5caecbe4fb814bf0531e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328863959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3bfc89de5afba55bd3e2aee5e74c1314a746444234b44ce14a7f3ab163c54c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615a40d637191fd38e803d020c6fd9ef07a75d9c895faae5c0a3a02afa988fbc`  
		Last Modified: Thu, 02 May 2024 01:51:41 GMT  
		Size: 13.8 MB (13767451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a1eba78863ed1ac0ba2415b97df6e0965dc6de515335030de35f5fb3b14c2e`  
		Last Modified: Thu, 02 May 2024 01:51:46 GMT  
		Size: 101.1 MB (101071033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05c920543def3b9e79c0dc987b6714a9bb228f24d18e3d6a2dd6992267570a3`  
		Last Modified: Thu, 02 May 2024 01:51:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8f7b6e5701292143797cca0c79a083febab7cf39233d60e3eaafe300415789`  
		Last Modified: Thu, 02 May 2024 01:51:35 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603a1bb653d1d063e21d09cb3a7f210348fe3bc3f49ea2196bbab626603e22e2`  
		Last Modified: Fri, 17 May 2024 00:13:40 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2b246981929d0106b28089f43030d96d783fa49463c4ad532580ba3a3ae86f`  
		Last Modified: Fri, 17 May 2024 00:13:44 GMT  
		Size: 55.7 MB (55666173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2b2032cbb3b5061d80261fdc314957f14cb7168e824583fb3b4bec19c0e08d`  
		Last Modified: Fri, 17 May 2024 02:35:52 GMT  
		Size: 122.7 MB (122730536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3874354f2f64c5d35a2d1c0c2bab6242901e1873ce3aa524867d1371f134c28`  
		Last Modified: Fri, 17 May 2024 02:35:48 GMT  
		Size: 35.0 KB (35005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:5829b1c7735ccb7288fb9e2a60fb7b9c00d9a35cd926ac21edf3acde2257aae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6996885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770e4dcb6ed4f2e1186587be58ee3620effdb32c1d991c997354f696049aaf1f`

```dockerfile
```

-	Layers:
	-	`sha256:bd5527c19174cbce1376fe2a7bc433918f1dbbd936059a61c31ac9ee76ef193e`  
		Last Modified: Fri, 17 May 2024 02:35:48 GMT  
		Size: 7.0 MB (6974623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8cd445dde7a8bd97379ab9cf2d4e1b84215cb5ea522a23950c4b8a169fb184`  
		Last Modified: Fri, 17 May 2024 02:35:48 GMT  
		Size: 22.3 KB (22262 bytes)  
		MIME: application/vnd.in-toto+json
