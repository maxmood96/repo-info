## `gradle:8-jdk17-jammy`

```console
$ docker pull gradle@sha256:06b674cf01c779cf9cd2eb7192c07f815f8071bc10852ba6660cbd9c7bd37e7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:8-jdk17-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:6cc83e622370515488fe50b6942ee74a34781ce200342c98f3a4e7be50336566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.2 MB (383202612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c51cbce8d0ac7ba1860001e1a1401712e6bd59cb065e81f68293521205de238`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
ARG RELEASE
# Thu, 17 Jul 2025 03:50:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 17 Jul 2025 03:50:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["jshell"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b800e9ed2b1b1b3965e771eeb813d79c1f546f121df420482937a05c2591a04`  
		Last Modified: Mon, 01 Sep 2025 23:08:57 GMT  
		Size: 20.7 MB (20700629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b1c9c3e5c947472f34a89126327af661d989ba1fb67f12a3e1771c7d782c9`  
		Last Modified: Tue, 02 Sep 2025 00:11:11 GMT  
		Size: 144.7 MB (144708986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d637b4327881dd7364f1374b2d8f361e76ee9530ea91cdf0c0bb719957d8c`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a2d920c7b851aebaf5aec59b861b624c3031d9e5e41d96ada370f8b47e512`  
		Last Modified: Tue, 02 Sep 2025 00:12:47 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420f3edce9e839fb77e73aa086fb2add423584809e1ba7fb0c0fcd326492627a`  
		Last Modified: Tue, 02 Sep 2025 00:12:56 GMT  
		Size: 50.8 MB (50799254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f6bf647d6ba834e81886d893dee7550311aae9b9973fe5e3710c10d6b4f196`  
		Last Modified: Tue, 02 Sep 2025 02:42:09 GMT  
		Size: 137.4 MB (137395129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c4c56aca1cae971ebe88134978aab70a5b4cff433003711bfa863ecdad112d`  
		Last Modified: Tue, 02 Sep 2025 00:12:48 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:4082d31e7424a110feca6c75503db60011847a58f514c393e19dd6b8fe0b47c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7883441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e4982401f5dc872e03f4bed4ed748c4b67b77fe8944d4cbae81c30a346964f`

```dockerfile
```

-	Layers:
	-	`sha256:14c9ff202a16e0419957554cff92f31f8c73c50376ed643c67e44ab5e4622a1e`  
		Last Modified: Tue, 02 Sep 2025 02:23:36 GMT  
		Size: 7.9 MB (7860667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3986944c077a4a6caf9b817cf0f8346e71ff72a045adbc2618892cfee5d874`  
		Last Modified: Tue, 02 Sep 2025 02:23:37 GMT  
		Size: 22.8 KB (22774 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:24a63be4acf27e3944ddb6a3a243bfe559ef603b5b8099d7afc1a04438f51197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.5 MB (380512495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2762c8f853326a935dc0d31e48a93deaa5fa14cc8766162aaf5d5f47726f446a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:7939f961de8cf091ed251aa1d8e432c16ec7506130ed39a1db4028efdad8fbfe in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:33392950d914bf1e16e980fc0bbcec6367a2d2b8ecbd726dc5fc65b4c96ce79f`  
		Last Modified: Wed, 01 Oct 2025 18:17:15 GMT  
		Size: 26.6 MB (26643435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471494b194dd6a4752a9e7dfe928fffa2f834cdb494689ff0f03c84e90151999`  
		Last Modified: Thu, 02 Oct 2025 01:12:59 GMT  
		Size: 21.0 MB (20989408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d41330dc934a932f2f6cd1187378525382e6dbcfd99c2689261665ac51bff2`  
		Last Modified: Thu, 02 Oct 2025 02:14:38 GMT  
		Size: 142.2 MB (142180525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2e35cb2b1ad0b5bf5d971b54f9c77d82e2f2ef6a99dd4a8de27e51818ee331`  
		Last Modified: Thu, 02 Oct 2025 01:12:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c905abe291db7795804d7cc6b78a4d7f97b148fd9f070a3987d9b27b4cdcf4`  
		Last Modified: Thu, 02 Oct 2025 01:12:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca032fdb60c8b0dffe3745483e78d4c22ac86bd8e90fb6c0faace3d94eae211b`  
		Last Modified: Thu, 02 Oct 2025 02:15:57 GMT  
		Size: 4.3 KB (4293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e1fde1b3d6acdfbf63ba9b490c2f0da0a958376cba420e1414e13c7e18081`  
		Last Modified: Thu, 02 Oct 2025 02:16:06 GMT  
		Size: 53.3 MB (53265948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d8a57f345de215c11bd85c89c2d22890009dc8193bee9c2434acf236b19ed`  
		Last Modified: Thu, 02 Oct 2025 02:15:31 GMT  
		Size: 137.4 MB (137395114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90132aeadabc0a134212e2e3f12708d7ba53fecdeeeeeac69bb864a2ba8b7`  
		Last Modified: Thu, 02 Oct 2025 02:15:57 GMT  
		Size: 31.3 KB (31298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:9fdea3398fcabd99045d0e468f381f44850fd6d7fe5bf931102ea518876a3ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7801838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116f71581a2c3834df868c5afeb5caa2582ece1ecd7f0b5a8448a6d642fd0d1b`

```dockerfile
```

-	Layers:
	-	`sha256:3d756afff8589fb4b18b2464a675f5b0b18379d12c3d5e9712a6a9befe2d5847`  
		Last Modified: Thu, 02 Oct 2025 05:24:56 GMT  
		Size: 7.8 MB (7778953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b58087dbfcfd5417fc6f0dadf6a128669ab29119ecdfe4b02acc33a266d02be`  
		Last Modified: Thu, 02 Oct 2025 05:24:58 GMT  
		Size: 22.9 KB (22885 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:56f95eb02626f48d01ef86b3c5f0c0ec3ba0802a2ea036ca52c49a9235e09368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 MB (380823852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a67a7dec2fc633c4836788c97dadb6573fa3a4709dec7a1f7e91d2eb6c007a3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e3b5c46cb782f51083cefe683a8b1730bc7c91e3a32ccdf998b3e421279f6`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 22.1 MB (22078611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1770528d7cc885ee03adb8564012d5818f73df6f98b42a92c710863bf282bbb9`  
		Last Modified: Thu, 02 Oct 2025 02:17:03 GMT  
		Size: 143.6 MB (143550922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1d35396ac9bf100ceac99dee6b2b90bdbebf883ccdc014e23b1820c3b2b67f`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709644d6a90ce830acdafadc19cca22af78d1a354f4572cdf9fce33f006eed51`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e788be2bb5989b265ddf331068c17786aecc55612bc342c254ac777844abebbf`  
		Last Modified: Thu, 02 Oct 2025 02:18:58 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fae87f19a020fd119f9de6514d0e381bd458af61d26884ceaee59a99c3027`  
		Last Modified: Thu, 02 Oct 2025 02:19:04 GMT  
		Size: 50.3 MB (50349708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75356debbcecb2cabef9fb757e93db9ecc9ca551b2c06c198f8eccb97647378`  
		Last Modified: Thu, 02 Oct 2025 02:18:28 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c73f856a206780073389935e1ef6bad574e717ec5859ba12b34a5413372c507`  
		Last Modified: Thu, 02 Oct 2025 02:18:58 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:d3dcc56396e5033d435af4b6b6b7c320be620414adb163ad509e7f0a5362e992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7985192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7c88b5735a3ba235f0d22f032814150ecacfeb33478d19e0089685aca266`

```dockerfile
```

-	Layers:
	-	`sha256:d9c4d4331dc8352bf0d34a4dfebee0ae4d14759cdbb17327eb673be833b7ca47`  
		Last Modified: Thu, 02 Oct 2025 05:25:05 GMT  
		Size: 8.0 MB (7962282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c8bbdedd7538e7438dc423d3b66101e098db7732668318278f377f85517ec37`  
		Last Modified: Thu, 02 Oct 2025 05:25:06 GMT  
		Size: 22.9 KB (22910 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:95bc231da233d43d853c547d267b16205b933acd518b039cbc3a4a157ee151c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.6 MB (393593586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb05f562f93f8618af99c38de58989e9dba0616cadb3a0ffb77d6ea6a8fcee77`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ac4f459c7226effc55c25655a772ab01a4267f689ebfa8bfb3d1cb2820e159`  
		Last Modified: Thu, 02 Oct 2025 01:29:24 GMT  
		Size: 22.6 MB (22582015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4b89fc5391729aecb7ecfb7147f4bcaaec161ce1247a698557f8fcb69fc115`  
		Last Modified: Thu, 02 Oct 2025 02:14:31 GMT  
		Size: 144.4 MB (144375689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c8ad123baabc3b27c03c1ab46db923e61efa1532111cd722c400df852a26c`  
		Last Modified: Thu, 02 Oct 2025 01:29:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813845beb8baa7ff5e708f3209eee5178f2ebe545dfca9f48a1c4d2a9d157754`  
		Last Modified: Thu, 02 Oct 2025 01:29:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945facfff851dd3e31f25391d194e0fa5a98c1245f1c385fc6c91a51f832d990`  
		Last Modified: Thu, 02 Oct 2025 05:47:30 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73249bbdad3fcd5eb6fa2856f5f77d60d94831f81b2060f0a40fab41520bae7a`  
		Last Modified: Thu, 02 Oct 2025 05:33:20 GMT  
		Size: 54.8 MB (54752095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c8437b3229ee89b6e21d877721ef2080fedf0cb259a2515316555e32dd49a0`  
		Last Modified: Thu, 02 Oct 2025 05:33:13 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823648d2dd16e7ec60ad0215a11b6f28bb21acbadc3ce696c2f2aa1ac9e524da`  
		Last Modified: Thu, 02 Oct 2025 05:33:17 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:082588388126883c6bbca2931ae7eb2b25db268d2c1b2b20591d26c5fd176970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7914329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18556a0ea359ae1f71a7b2811e96c0f96ae799fcdf955308e36bd247b842dc9`

```dockerfile
```

-	Layers:
	-	`sha256:c12c6edb88e1272c1898440a2ca6146cb417d6a9da4a596834aa6b435f826175`  
		Last Modified: Thu, 02 Oct 2025 08:22:30 GMT  
		Size: 7.9 MB (7891511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404f67a772af63445b3d1345fdada6326160e5b3c5dc82468e7d2018d5f69e98`  
		Last Modified: Thu, 02 Oct 2025 08:22:31 GMT  
		Size: 22.8 KB (22818 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:770d37c0408a27f094be87acb9d0c352ec483b25215e04ad21c39dc98f39bc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371082902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c8b748cc5fb14b88e92efa5e36574fab806fe15816bd4bc16c2c25fa07425e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5db983e1437101247e4457123304ebfed1b2f5bda55689e0208bb26f3ad06dd`  
		Last Modified: Thu, 02 Oct 2025 01:18:11 GMT  
		Size: 20.4 MB (20415506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01064a09ae3eea683cefab3ace3a94ecad0efbc56b6589b0a3b9e3a3454908cc`  
		Last Modified: Thu, 02 Oct 2025 03:25:14 GMT  
		Size: 134.7 MB (134729904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cba681e9147f25abf7a30df0db14bd447a52d88e3c8f777722b6afccb960a9`  
		Last Modified: Thu, 02 Oct 2025 01:18:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c1bb6966c23a603456fb1e2e47ee55c9c6ad2671113330131b455587585d16`  
		Last Modified: Thu, 02 Oct 2025 01:18:10 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558550f019fc9661e91e7ac83a06610a5c9e7a11b5e4bd42e08d054b9b504b8d`  
		Last Modified: Thu, 02 Oct 2025 03:06:24 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f845c361d1842fe8f740046fd5d33821db8f4dcea784018a5687acb5765d5f3f`  
		Last Modified: Thu, 02 Oct 2025 02:55:20 GMT  
		Size: 50.5 MB (50497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8b31e814f113b06fcea4440b38956992a9d8566a744c14b8d757e0323125e0`  
		Last Modified: Thu, 02 Oct 2025 02:55:22 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2769c302c799da488393734da277e577f1346ced2d7ddb16eaa1edcd427acc27`  
		Last Modified: Thu, 02 Oct 2025 03:43:58 GMT  
		Size: 35.0 KB (35003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:6240063779277b382b2c971888c31effb9ab3904fd32eb747f2239efb935c072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7807121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04aaffde8b7969fa4f004b738b3a7fa6a608255a50df7b17147c6da317e5ecb4`

```dockerfile
```

-	Layers:
	-	`sha256:4df41eb8ada001ad1c13bebd0e73ec7977bffaac0cdeecdaf43bda5bc25534e1`  
		Last Modified: Thu, 02 Oct 2025 05:25:18 GMT  
		Size: 7.8 MB (7784347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68242c14d4e0f6b2db218dcc8a6d63bbfa9ad02169b75fd736909fcf0065f2ea`  
		Last Modified: Thu, 02 Oct 2025 05:25:19 GMT  
		Size: 22.8 KB (22774 bytes)  
		MIME: application/vnd.in-toto+json
