## `gradle:7-jdk8-focal`

```console
$ docker pull gradle@sha256:0cf443b469ec748f2187186b4f4b41df875da77590fbe164242c762aac738464
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

### `gradle:7-jdk8-focal` - linux; amd64

```console
$ docker pull gradle@sha256:861f7d9dcf53481f0be61a6baa57287abf8d5c3a34b16a04a00d2103393a09dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 MB (336346249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837aa24193fcf8beba2a9522addec42ddbd9f9edfb07f6da0f232438ab0f6b6b`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cd9d4a2e5127a445fb954ed8ae9a10638fd2683d42e6285a42f444339287fd`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 16.9 MB (16931696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0389810377a45ce532f9352adc963667be22583a004c54c1baabfcc72385c6`  
		Last Modified: Sat, 19 Oct 2024 02:06:34 GMT  
		Size: 103.6 MB (103616508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d198e8a08206363985e6e110314597fd737c32514fc6225a112057dce626d5`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4624c98b78519a076d734e8e7b5160858ef8ce0b94a971970379d5ccffd6e37`  
		Last Modified: Sat, 19 Oct 2024 02:53:25 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9bcd0ab8bf2abf25bbe6284b6773cc19477bd96fb5b03178e1ed5df8133417`  
		Last Modified: Sat, 19 Oct 2024 02:53:26 GMT  
		Size: 65.5 MB (65494959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa924bc563ce6bb5d78f25011221c9a6c84b9c7396558d2b36f02b349db6a78f`  
		Last Modified: Sat, 19 Oct 2024 02:53:27 GMT  
		Size: 122.7 MB (122730527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715e88fad8a0f1049b55fac55cadb45f74499977610900e7d48d0105fef773aa`  
		Last Modified: Sat, 19 Oct 2024 02:53:25 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:6148f55aa7d4ca83f9552e9736c9a1ac8d38c5bee8c6004a8692d6aacfefa63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7748915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a5a871db838e82496a313c2771d58b53399aad70cb96463ba49efef74739d3`

```dockerfile
```

-	Layers:
	-	`sha256:02188be14daa84874eab95ae8930cf43b9888c4dcdf13b0d522a69193ee6ef6f`  
		Last Modified: Sat, 19 Oct 2024 02:53:25 GMT  
		Size: 7.7 MB (7727521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70dbf2a2e9242934de8bce00a55d053ffb3f314a1b047437e924e5b872b769cc`  
		Last Modified: Sat, 19 Oct 2024 02:53:25 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:e1ccd5e71a180298f780d1f56fdbd69be5e750558d7d29aa313a1a4bd3ad789d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321229364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddc89084d1bfc5fa94bcc5ff9d5aadbbc6d7e4f3adc0cb947197c4e0896c843`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6da1c0cd70ff8def0afc476602312ab72c48c692e501fb298e735407a9759`  
		Last Modified: Sat, 19 Oct 2024 06:49:10 GMT  
		Size: 15.7 MB (15678763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdd892a41eea81b99f9f99c02cfe24243fbdc2d810df3cd50c9af70d1b2d156`  
		Last Modified: Sat, 19 Oct 2024 06:49:12 GMT  
		Size: 99.0 MB (99011695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff75ef08a28022889670a0923b7d89cd8b1ab2b41657a382c753707775741878`  
		Last Modified: Sat, 19 Oct 2024 06:49:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc698ad93ca176271fc0a9bc65620555214bf45d8553720fb1eb587c1d2b475`  
		Last Modified: Sat, 19 Oct 2024 06:49:09 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69daedef2f2de562d8572e4b27d14e47849fac9f6141223f2af638f09f21f24`  
		Last Modified: Sat, 19 Oct 2024 08:30:29 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113e46e1dcb4910a0feed7c2fb3c02787ea39d5696eef5c4c782fe4359a09581`  
		Last Modified: Sat, 19 Oct 2024 08:30:31 GMT  
		Size: 60.2 MB (60150090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170714ecbf79943c570b88049f8b368a0009d8aad75fd6301aeb550c014e1dff`  
		Last Modified: Sat, 19 Oct 2024 08:42:01 GMT  
		Size: 122.7 MB (122730526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f340426b8dd90a5ea172a36713172180cf0511d6b27513f736527a825ca5c8`  
		Last Modified: Sat, 19 Oct 2024 08:41:58 GMT  
		Size: 31.3 KB (31294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:24e1e24a396a726442b05b8dd8aaf2d1c549845eb3747c46bb8eec5bd09c6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b13b5f5f2fb4613b86d3ae2b7ad3b6c69a551fea2e016a856ae640fd0b106e8`

```dockerfile
```

-	Layers:
	-	`sha256:85e6a14e6674477e603b60bf2dc198e0e6809612951889698163a994a2072ff9`  
		Last Modified: Sat, 19 Oct 2024 08:41:58 GMT  
		Size: 7.7 MB (7732721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd48994ce3aca5399fc0358ac51c770a8952d64712aea384f411a651f61f3c`  
		Last Modified: Sat, 19 Oct 2024 08:41:57 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b0b76a48d6ca4ad5ab5745bd57b2ed8e05db584e43e782e67f269528e3f97e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.6 MB (333583847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62158a83896dec8f8d3d68a866069a87a031677a703bebf4f5d00ba716efb753`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ea3750e5af5cc1b8b30ad4f703c164de67b1bf83f0d94ddb97346bc02fbcf2`  
		Last Modified: Sat, 19 Oct 2024 05:26:21 GMT  
		Size: 102.7 MB (102734092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887875d5a4385da1870827c54b94fe28a8a36a0a2a6180267ccb0e7b62c8d038`  
		Last Modified: Sat, 19 Oct 2024 05:26:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc239a0dbeb97c950d05f9ece6229754e73388d47ca1b5aa7cf489091ae596f`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d657cfa3e2e63420d7f09d3cbef556c834492a7aaf64b4b97357243bf94c6`  
		Last Modified: Sat, 19 Oct 2024 07:02:11 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6260753ff7ea96cb964f0170bc230e8d721bce8cad643a6380755d5d358cdc0e`  
		Last Modified: Sat, 19 Oct 2024 07:02:13 GMT  
		Size: 65.3 MB (65291687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d589fdca0451341030e949427e8f4d564f0f9c609b5c6c52002295dba2f1f946`  
		Last Modified: Sat, 19 Oct 2024 07:15:46 GMT  
		Size: 122.7 MB (122730526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449cbc729eab04e4b6a4c1f009fbc3bb50ce7dee075d45976c313df6de04e35a`  
		Last Modified: Sat, 19 Oct 2024 07:15:42 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:9f6bd67335ddcc0d3a24895575270a9ad84b790e16a6969062bd058ad3f2d6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7755575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01291b0ec43d38e96f556375f5ae8f13411bb09ce02f1b81c9f19b630e80fb5`

```dockerfile
```

-	Layers:
	-	`sha256:8675c6b15ef50630083cbaed9ff80a31b2b91836cc44db36ebd4f07495a0ef31`  
		Last Modified: Sat, 19 Oct 2024 07:15:42 GMT  
		Size: 7.7 MB (7734042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a615573247ed669761387edc46ef6613414c0c95172c820ce66d80a738a1597c`  
		Last Modified: Sat, 19 Oct 2024 07:15:42 GMT  
		Size: 21.5 KB (21533 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:e9cd8fdba8e78db694577f6c94d5cd1f3242a4262179e8ed1baf1cb3dd9a735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (348027763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d654126f31d319f5a638528f321c0d1b6f57c796bb105c64ee0ffc2243bcda`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
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
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d82d180d2a71e9810b37a59c605f26d958a89f42ca8d64d57bdd44918cac352`  
		Last Modified: Sat, 19 Oct 2024 04:17:06 GMT  
		Size: 18.2 MB (18240226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520499aa273eb77ab03a0cbbe65d9bea1e87b19829a0a892fc873fc321ab3239`  
		Last Modified: Sat, 19 Oct 2024 04:17:08 GMT  
		Size: 101.1 MB (101080653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db12569144839a0745a247cb6d93cd493a04352cc19cef327a257e428b2a19b`  
		Last Modified: Sat, 19 Oct 2024 04:17:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae5237d320f173db6ea4397e2d296f0187972304fdf4a4110a685122d3ee1d3`  
		Last Modified: Sat, 19 Oct 2024 04:17:05 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3278fb3a548cb3ec2193e36e5b016d2371ba43ae64ad414bad705c9b3d4258ab`  
		Last Modified: Sat, 19 Oct 2024 05:40:06 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c1f128747659a8d3b0b5552479a697ae3d69c9ad01971a953b836d6495ab3d`  
		Last Modified: Sat, 19 Oct 2024 05:40:09 GMT  
		Size: 73.9 MB (73858234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6099552517d1ed554d0270a19e1767aec6c24b618f1660d4a5aa230b3fe91c41`  
		Last Modified: Sat, 19 Oct 2024 08:59:51 GMT  
		Size: 122.7 MB (122730528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5773eeb6caf53725d9d1e5b699aaf1695f3045b69ae82172f8e6fb57d51da284`  
		Last Modified: Sat, 19 Oct 2024 08:59:47 GMT  
		Size: 35.0 KB (35014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:87e3ad6c0cda3fb5921e7a1818806b9836187ac4cce827a0a4aa63924266732e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9296940a138acbb78b8eeafe48d2b00718c1f3fcb7db9fcc77b8e9250da73c50`

```dockerfile
```

-	Layers:
	-	`sha256:6dd9191209ce4935b124008a7aa01666ec6ca045876a0194cc68a839727dc815`  
		Last Modified: Sat, 19 Oct 2024 08:59:47 GMT  
		Size: 7.7 MB (7733456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc865173a36f0ccfca360d60960b23b69f8336bf482892b60112998aa9cb06f8`  
		Last Modified: Sat, 19 Oct 2024 08:59:47 GMT  
		Size: 21.4 KB (21440 bytes)  
		MIME: application/vnd.in-toto+json
