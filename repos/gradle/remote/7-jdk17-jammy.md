## `gradle:7-jdk17-jammy`

```console
$ docker pull gradle@sha256:a45447d900d4fa49efbe31a757892a054b587c60c55c1e143955481ce36e6dc2
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

### `gradle:7-jdk17-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:ef979080fea5ea82ffc8697f85ab171d8c5e17b691844a3a3d9194c903859e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.6 MB (370637877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96727a4410529da16975d4c0fa076935614a48c3ea9fcf938541acb67ac312d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:23:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:23:11 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7575fa115e62f663c8e530c448272a4f4dde81c6f5744b8ba99d3dbfa5671d2`  
		Last Modified: Wed, 23 Apr 2025 16:32:06 GMT  
		Size: 20.7 MB (20693830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5c220288dea1cf3e5d90e266c084b0c2e42da563ec1b8953b5142be498ff2b`  
		Last Modified: Wed, 23 Apr 2025 16:32:08 GMT  
		Size: 144.6 MB (144646773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7164c6fee456ad2ff449de6a87782c809fca0c9e2e7d1e73b141c603dcd8f00`  
		Last Modified: Wed, 23 Apr 2025 16:32:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0137fea4bef4dc4ff919d973a8ae36f29edacba15f7b5129ebe177983d665fe0`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f51e45162e27349b0c3aa5ae8119104b64987be5c63ee2bd3c2d606832409c`  
		Last Modified: Wed, 23 Apr 2025 17:10:36 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a95e0872bac22419e64f2857ffd58318ed29cd4d54c01b60dec4757913d09`  
		Last Modified: Wed, 23 Apr 2025 17:10:37 GMT  
		Size: 53.0 MB (52972690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f399293dd704f748361271f9e9db8fe76da3ef1ef7eaf04996a7230d473ed806`  
		Last Modified: Wed, 23 Apr 2025 17:10:38 GMT  
		Size: 122.7 MB (122730531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0fbdbde84c63a6af285d1ed1d9084c104874ba9c791f0d5457ca0e337bc51`  
		Last Modified: Wed, 23 Apr 2025 17:10:36 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:232e991d6cc65dac1914d873b2fa9b8b9476d19ccf75397f4ec4e4027e563d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f55e20c8da3205f75cd7e32cace2ded7eea91cae15c90f8da08016d7194e04`

```dockerfile
```

-	Layers:
	-	`sha256:70791beed77d6a451b34f44514af53ac20587010c77bbda6d10412cc4df4591d`  
		Last Modified: Wed, 23 Apr 2025 17:10:36 GMT  
		Size: 7.5 MB (7497835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c1355891b6a64fdde8b3b8e6040c87ed81c9a7b12325e9b0995e523e1cfbd7`  
		Last Modified: Wed, 23 Apr 2025 17:10:36 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:4d825b297e002766a1cc00fb82c3c72d0badb43e28deb8f60f51a241248f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365681409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d6022ad2bfdb207e10e1e326e4c61f5d29c956f326a4046ea28da9b68c53d8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:23:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:23:11 GMT
ADD file:0644b965bac173b3de427d73c19d20e4fb61d50785a17a303e350f86b7865f26 in / 
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:bbd8385a156b4afe216eb6b84f86bc7178bca4ab42ae42bb98f3576ca9f4e17a`  
		Last Modified: Mon, 28 Apr 2025 10:43:57 GMT  
		Size: 26.6 MB (26640827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cf0ffcd11b616a815412db1d2bff041f71811d4f309c91b8970835a52450be`  
		Last Modified: Mon, 05 May 2025 16:42:44 GMT  
		Size: 21.0 MB (20988777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8694365b4cc1e125c5b98cb3efb56cfe7e7dd40ea73d72c2d56427b84264c382`  
		Last Modified: Mon, 05 May 2025 16:42:47 GMT  
		Size: 142.1 MB (142121687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e94ec0b7b08ddb69c790b66656dfd1642dc9a05e671666b301cc1579fc55ac`  
		Last Modified: Mon, 05 May 2025 16:42:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356e52b736e1b4571a2c700fececb5dbba80f5458ab4bd0eaf3f2f31e0f9292`  
		Last Modified: Mon, 05 May 2025 16:42:43 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c8d947912878e281a9f6611a6633b829e3e41844aed4ad41d9d376bc9760bb`  
		Last Modified: Mon, 05 May 2025 17:06:12 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9733634f38cc50cf3a1bbc895c379b7534ee33c511122dd3106703347f5b9a`  
		Last Modified: Mon, 05 May 2025 17:06:14 GMT  
		Size: 53.2 MB (53161507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eea64cc24ac9897455abc88ab899ee7a0f470f8359188cf9835d823a460c0e`  
		Last Modified: Mon, 05 May 2025 17:10:37 GMT  
		Size: 122.7 MB (122730538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47b8d50391d14dffae15eb976cf4db3ce40cadaa660f1a06bbf7c52e73eedea`  
		Last Modified: Mon, 05 May 2025 17:10:33 GMT  
		Size: 31.3 KB (31301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:cc6f98276ca4e9c83263d7fad08c20818c8a3698d62f143ee4d52aa046d147c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3af349c3e0312f9e62c1399769b97e65ba0b1d36c7866f492b5a3061bae19`

```dockerfile
```

-	Layers:
	-	`sha256:035f8ff8c379882ab3e399da4a9e8c964b5ae1436d939dfc817a5dc756be39de`  
		Last Modified: Mon, 05 May 2025 17:10:33 GMT  
		Size: 7.4 MB (7416162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:378b00dbeb58fc26994f0b6ac63f8c7a086035195adf167d788e306f8b3cfe21`  
		Last Modified: Mon, 05 May 2025 17:10:33 GMT  
		Size: 23.3 KB (23257 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1b6ffc259a183c2413e551c71dc14519ad117c929238435a2f1b5d00fcfa2f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368200395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f63da6952da458027737c96a0c5c9f0c347bcb8e8d1c86a1849003c22e06c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:23:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:23:11 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b14141c255ebde08ea2dc9ff81289f3fcec02625983b6981b076ad4ae3927b`  
		Last Modified: Wed, 09 Apr 2025 07:04:42 GMT  
		Size: 22.1 MB (22069470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966800e8635a1ca13ef064688a406dd4d9e1586b47b05ec84a24e3c6b2ae6808`  
		Last Modified: Wed, 23 Apr 2025 16:36:18 GMT  
		Size: 143.5 MB (143512496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca0d1f21e46c96a0458e71c91a601408e944bbf262536a187f6e4e82cc0024`  
		Last Modified: Wed, 23 Apr 2025 16:36:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fbd5441388ada2bd61d783b3f56b9ea0a6c5656aa9386551d64fcc39d53f90`  
		Last Modified: Wed, 23 Apr 2025 16:36:15 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6a62075eb5f31fc594633bff249afde735180176014fb32d1a63978ecfe718`  
		Last Modified: Wed, 23 Apr 2025 17:30:19 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571a8bb5890cd222b8c8b234be9e36ed6a34dee9af358dd45befa81bd649813a`  
		Last Modified: Wed, 23 Apr 2025 17:30:21 GMT  
		Size: 52.5 MB (52467358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09cfe2aed47a093d33052536f98f13a9b51d96f64d8684870cf7b5034b85c0a`  
		Last Modified: Wed, 23 Apr 2025 17:38:57 GMT  
		Size: 122.7 MB (122730531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bfeb1938ec6bb7e604ceaec06a48b9f553dd2fccb4aa52a5fff30b9fbcfbca`  
		Last Modified: Wed, 23 Apr 2025 17:38:53 GMT  
		Size: 59.5 KB (59519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:222015b9d79dfde83637f6d53c2f682203db32e73f44b71d2c9e7a328f27e8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7622828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d25806462a39d14ab81a79b99b5f2589a18a69d94654a88ab69187298208ef`

```dockerfile
```

-	Layers:
	-	`sha256:41b8a9bda8e18fcd1ae26ea473ee225dec319071fbfe87e57a809212525f5de7`  
		Last Modified: Wed, 23 Apr 2025 17:38:54 GMT  
		Size: 7.6 MB (7599517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb709beabcaa44764e06d0c0f07a30f3b8a4c6eb01c20bf7a255ef23ae92b89a`  
		Last Modified: Wed, 23 Apr 2025 17:38:53 GMT  
		Size: 23.3 KB (23311 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:39c5cb735de602426956832ae22da66a10eb433e1af435aa7059e6796782336a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381134177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d556313233e875d42bd1792859155ae01a549bdc2f508ee15d1ac015452d4af`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:23:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:23:11 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5393a4773f758b6a98290f1049261da58986973d290a6e694de54f203243d455`  
		Last Modified: Wed, 09 Apr 2025 04:46:41 GMT  
		Size: 22.6 MB (22580774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de95e57f517d9701ea33f49fc104d3d3cf32330b26ee4d512aacd93d732078c9`  
		Last Modified: Wed, 23 Apr 2025 16:42:25 GMT  
		Size: 144.3 MB (144288979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b82f7d7e688c46b4d6d3d80f8656245f5f4a0679cef69186fbf9ac82a8c8b5`  
		Last Modified: Wed, 23 Apr 2025 16:42:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec2634f1c539a4cbfd92e273bca0aae4849507318abd17192e3c76d3e207c7`  
		Last Modified: Wed, 23 Apr 2025 16:42:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898bed827a24ec35c56b57642355656e72e477522a684d81de273ec66eda1576`  
		Last Modified: Wed, 23 Apr 2025 17:20:55 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e726275d5b9fbe1040abc3b9b0230451ff4c4400cca77c8663523284aaf1f4f8`  
		Last Modified: Wed, 23 Apr 2025 17:21:02 GMT  
		Size: 57.0 MB (57049407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a2ee9961d3758e978b942e005ff08bd1f2e1947a7b819e4942bc8f6833d8a`  
		Last Modified: Wed, 23 Apr 2025 17:36:00 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ab250f40645e8abad741e3fbb2213ffaa894bc76b0dc4fc337133f7b14688c`  
		Last Modified: Wed, 23 Apr 2025 17:35:57 GMT  
		Size: 35.0 KB (35005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:0bb55c6bd73467c668527053349f01fde1cdd0b216fb85c3390e14a851854d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7551697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaa6d6fabbe96170370b0e11cda7389e0586fe4db1240f32754a71ff8e4888a`

```dockerfile
```

-	Layers:
	-	`sha256:134fc4931de7ebd7d79be413b4f45f50b547a89d063ba8111b4899bd470be4f2`  
		Last Modified: Wed, 23 Apr 2025 17:35:57 GMT  
		Size: 7.5 MB (7528514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ce8c280589aa535574618f102d7117e783ae2592fcf483d313679d78eadfe`  
		Last Modified: Wed, 23 Apr 2025 17:35:56 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:918e9513cf98b51127373646593c0636be85edd643995e5532e796ccaa1d4d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358568509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e194fc899661c5159647478e8937a58f3bd510de083c3019f663eeb6660c547`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:23:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:23:11 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:23:11 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a659edab8d87ca08491fe070fadb488a06d2ef855c0cda299c9132cb70ed53`  
		Last Modified: Wed, 09 Apr 2025 04:21:00 GMT  
		Size: 20.4 MB (20412803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264e17d8e95b7ec11468767be0b6a9203250019433fc04a1359e3fae8033475b`  
		Last Modified: Wed, 23 Apr 2025 16:38:05 GMT  
		Size: 134.7 MB (134680767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7261d0553c0833d66f44f90fbb7035df4045f14a29761278d2772ef888995bbb`  
		Last Modified: Wed, 23 Apr 2025 16:38:03 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b0813dcb53fcf0b98a919eaedbf654a0f99f51abe2156b07803b5c9345af7a`  
		Last Modified: Wed, 23 Apr 2025 16:38:03 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c4cedd2e17de0618b31c80cbba0bb6a6ea566cb41475d3b5d962273094aba`  
		Last Modified: Wed, 23 Apr 2025 17:15:31 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b76bfba044f6c157bdba5c39d05746931462f3dec9c96f59773c6e14d1c342`  
		Last Modified: Wed, 23 Apr 2025 17:15:32 GMT  
		Size: 52.7 MB (52702496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9503d5fe2b9cff77646550016bad19dcd269274294e867fb436b66a32fb7d85b`  
		Last Modified: Wed, 23 Apr 2025 17:24:53 GMT  
		Size: 122.7 MB (122730531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e679a34f340332df6a2e5d60772d67681882e34bd7fa6f092b7098d4cfe759fe`  
		Last Modified: Wed, 23 Apr 2025 17:24:50 GMT  
		Size: 35.0 KB (35004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:efe9e75fdf77907a2199da91878a5735841d139ea1ac0138e844e312ddf86d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa39170b9c163bcb55f86add18641d870fb5836603c80c830eb572f7cdb5db1`

```dockerfile
```

-	Layers:
	-	`sha256:35447d49684885b78fe0b7dac532454710a491de81efb9fb1c1f897c8a47d2c7`  
		Last Modified: Wed, 23 Apr 2025 17:24:46 GMT  
		Size: 7.4 MB (7421512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a0463b2d1160ed01ff97dcd76a1a53c272aebf73874c7ec74f23fa66aa6c86`  
		Last Modified: Wed, 23 Apr 2025 17:24:46 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json
