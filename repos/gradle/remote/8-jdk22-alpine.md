## `gradle:8-jdk22-alpine`

```console
$ docker pull gradle@sha256:3ae8a53d413a5cfd6fb474b28e4033c124660796a3297dbf80213d108367e1a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk22-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:7dd65d0dbf0b49e31faa071a42ac4479e0a4dee224dcb70389475c4e611da022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344509784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15312841147e2dc46b85b6ac0adc71010d6c639bf051eb7ab647fbd935639b4d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 12 Jul 2024 03:13:38 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='86a7b47c9277f2fd063ec910616b3676d86553ab7d23aa3bd365e51a57be1dc5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|x86_64)          ESUM='d226e44b3513942db855df9a8737d848f64069848970d4cfd35ee3c38f2525c1';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecebdf4c53e7de19c31166ad7b858f4092b5f6069fc8023c805472b84acd7ef9`  
		Last Modified: Tue, 23 Jul 2024 01:11:56 GMT  
		Size: 13.1 MB (13142483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c9569005e30bec9080af61308d58651a68f6beada8f2ca3245fe7a59f2eaef`  
		Last Modified: Tue, 23 Jul 2024 01:12:06 GMT  
		Size: 156.9 MB (156934767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386464ce9ef7ff1ed6c66122df7cdd506c7470f0b50d812cffd4e069e4828630`  
		Last Modified: Tue, 23 Jul 2024 01:11:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165747668724c2aec1d076a974921837b137b99779ef988b5aa5bde3b2819abd`  
		Last Modified: Tue, 23 Jul 2024 01:11:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d97de10555c75805d049d3894d67d913fe3dca0a93bc17aa9102082b096bbf`  
		Last Modified: Tue, 23 Jul 2024 02:01:12 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db834edb3ff0c9b4e4e4ddbf83572678271ac22d4f08da675f4654dce1819f20`  
		Last Modified: Tue, 23 Jul 2024 02:01:13 GMT  
		Size: 34.9 MB (34878928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f36979a592b4b988d26e3f93e1a52fa7df05281e60a059bfc3d86fbec50c4e4`  
		Last Modified: Tue, 23 Jul 2024 02:01:14 GMT  
		Size: 136.1 MB (136132066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3780f5d3f062e87ec8154286ca22ac7a5c01b578cb15641dae8d411ddf2201`  
		Last Modified: Tue, 23 Jul 2024 02:01:12 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk22-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:420bd8ab9d3c0539a5aad4f97b89ce18e343a1c0c52c62af68882c5491e69aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3504385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6728fe9daed82a652ad689705d6de0ef8632bc1dd3a7a29861d5f748c362996`

```dockerfile
```

-	Layers:
	-	`sha256:c07a8e62439b94eb9ae0ee61107e5cf93078db7087d316b168229f3628dd462e`  
		Last Modified: Tue, 23 Jul 2024 02:01:12 GMT  
		Size: 3.5 MB (3483518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c539a8d7771a143a4007d96c77ed7749615ca56e4bd01c98731865a4817b52`  
		Last Modified: Tue, 23 Jul 2024 02:01:12 GMT  
		Size: 20.9 KB (20867 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk22-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4665533516cf37b289a60c6ed44fb93dd8d29e984c8f7cf07a99afc6c696981d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342515978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3011f0015efed735912a01c911b8a19a6da1db5e1ea9937c84bd9d7d62a44c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='86a7b47c9277f2fd063ec910616b3676d86553ab7d23aa3bd365e51a57be1dc5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|x86_64)          ESUM='d226e44b3513942db855df9a8737d848f64069848970d4cfd35ee3c38f2525c1';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db88ea1e6a26d6517be6a6098be6964b10513b0bfdfea893bc9752c9c04b6e1`  
		Last Modified: Thu, 20 Jun 2024 19:04:39 GMT  
		Size: 13.4 MB (13425513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841f000ccef53501d82609f3a34d8619adf66a18d130d92c5a8217965c0b7617`  
		Last Modified: Thu, 20 Jun 2024 19:05:26 GMT  
		Size: 154.7 MB (154683674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248f5f9cff3f5ddf16e1a9197215b686b5158aaf73558f5ef41009be0b370f41`  
		Last Modified: Thu, 20 Jun 2024 19:05:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a9ed642476352fe117f93e090c36224adc59894662b7e86ec03db3c520d3d1`  
		Last Modified: Thu, 20 Jun 2024 19:05:15 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63827bfb832ebc006c7cc5907d04dd39c03d3d3c415a608fc21c9daca7d36cff`  
		Last Modified: Fri, 12 Jul 2024 18:15:25 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6201decbd50819222ba5cffaef7bb44ab469c73cff57527b150fbc0b82d0a1`  
		Last Modified: Fri, 12 Jul 2024 18:15:27 GMT  
		Size: 34.9 MB (34914973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cac1e652f11c3ec7aed80367cf1d09fbfe5dcade056688f2f0755510c56c14`  
		Last Modified: Fri, 12 Jul 2024 18:15:29 GMT  
		Size: 136.1 MB (136132110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793ad00373c1cab1ec8085d5a355641fd9240ae459351e6668ea4f23d7f4e7a`  
		Last Modified: Fri, 12 Jul 2024 18:15:25 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk22-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:98cde47f7ee9e8e5ca034b5a8ef9b864de1a1faf50c9b9ae210fa57071deaa8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ce5add146dd731cabace4ac8495cb7bdb65e284e058c8bda815bfaf1e7608d`

```dockerfile
```

-	Layers:
	-	`sha256:ab1e877da480a44db6546f9bd05764a187952b20f9e675579defd16f170b76bf`  
		Last Modified: Fri, 12 Jul 2024 18:15:26 GMT  
		Size: 3.5 MB (3528207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc247ecffa2806194d4d1d256655ad1f549176c4bbf0fd4baa1179bb59b197d`  
		Last Modified: Fri, 12 Jul 2024 18:15:25 GMT  
		Size: 21.2 KB (21185 bytes)  
		MIME: application/vnd.in-toto+json
