## `gradle:8-jdk23-alpine`

```console
$ docker pull gradle@sha256:0c86728d97fd80f52a10d0f317ec33e182a0c66f1c1aa18b50da03cb6fc2a01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:ee1835aae25b188d9c6f39e7e6d8b4e69ed21866bfcabb42692cfd9cb0ebfdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.4 MB (359355642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683dda0fd66c5a95cbfe53ed7dcc0b7cde5f7abf5ae60f3740302ad5b0bd9419`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Feb 2025 02:49:08 GMT
WORKDIR /home/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_VERSION=8.12.1
# Thu, 06 Feb 2025 02:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER gradle
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER root
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229c05d87edca42fb39c5ffcb5e0bedea7fa96b9bad361c3f485d50d3924db86`  
		Last Modified: Fri, 14 Feb 2025 19:25:53 GMT  
		Size: 20.9 MB (20949783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b130aedac2651a9435f8d0805a2d5087c15a9d5fad2bd2530fe060ed83a2e3`  
		Last Modified: Fri, 14 Feb 2025 19:25:55 GMT  
		Size: 165.5 MB (165542654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2074c3edf5c3e5f9ddaaa783c5b33ec8f9287af1909346c4f90103a9579dffd4`  
		Last Modified: Fri, 14 Feb 2025 19:25:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c67efadec52153c3e21caad3dc817dc99704b643bec8d9324830842d5d29b6`  
		Last Modified: Fri, 14 Feb 2025 19:25:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1987020abb9d4b536a30c3f580cb20d57f77f50ff5499ab26371c95b102b0e1d`  
		Last Modified: Fri, 14 Feb 2025 20:35:40 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd83abb783f4e51af7ec72b3d3b2c921b824322008e870ff8919b64080215af2`  
		Last Modified: Fri, 14 Feb 2025 20:35:41 GMT  
		Size: 32.6 MB (32600563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd4a834f5c71a99e64b4481f8f288ce8d8ea8f90afd0e3158144e57af6f3e82`  
		Last Modified: Fri, 14 Feb 2025 20:35:44 GMT  
		Size: 136.6 MB (136562037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00fc0d26d180f504256c31fe00ed5c2e637b6b1fee51f73ba2af5492140b58`  
		Last Modified: Fri, 14 Feb 2025 20:35:40 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:0c4a95b7cbc52f95d77b3f16b70db196ea8414653b63dff6cab613f6c8b7c607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b503950b1ea5ad63749914db1d32d587f8fe83a22cbd9d260a6c3c166aefd102`

```dockerfile
```

-	Layers:
	-	`sha256:b587f1c2c5e7d30f343af5a83373bacabc1b9eb98603af0b3f5529c8758f9cd9`  
		Last Modified: Fri, 14 Feb 2025 20:35:40 GMT  
		Size: 3.4 MB (3351173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79a32d46575653fbdd32842368055c7b10cbf96aaeef3e04ab542dca8397e19`  
		Last Modified: Fri, 14 Feb 2025 20:35:39 GMT  
		Size: 20.9 KB (20912 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:97108ee5b7d3c67902c80b1dadaef846e26b5b54934733df76a74add468daa4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357234051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f852b8bb666afc6b1d26c63daccbba51e540b9c2099ffa23aa1ec0f90aaa32`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Feb 2025 02:49:08 GMT
WORKDIR /home/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_VERSION=8.12.1
# Thu, 06 Feb 2025 02:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER gradle
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER root
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22460361c4e9e1ac6bf5bc45209d88abdf89352662d6ea415fdaae2281c39acd`  
		Last Modified: Fri, 14 Feb 2025 22:43:26 GMT  
		Size: 21.0 MB (21005533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15671aa80e7a6e436c07484000d6383de4e016bf170c960be0eebd90ba1e8390`  
		Last Modified: Fri, 14 Feb 2025 22:45:41 GMT  
		Size: 163.4 MB (163380052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080fbb5481fba57cc68be14a8b64de610c22ed61e64d96b8b4612865af241d87`  
		Last Modified: Fri, 14 Feb 2025 22:45:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e44c032ddc6f6b57aa8bdaa1d07ac948ba70c708aa8a9e3cd69617041fc1d`  
		Last Modified: Fri, 14 Feb 2025 22:45:37 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ba85ac99b1db6164aa07c2d7970676c920ae52ac8e42d37bd59d1dd7b3ed84`  
		Last Modified: Sat, 15 Feb 2025 10:22:29 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657b8d82d2c7de9f670e1e551b5ced221d4db2b1e0ea24facbcf4a6c5505c3c`  
		Last Modified: Sat, 15 Feb 2025 10:22:30 GMT  
		Size: 32.2 MB (32230414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e4b2a676edbd0140444875c1bf6d24774c2926db9946cf76c7f46e029d88c`  
		Last Modified: Sat, 15 Feb 2025 10:22:33 GMT  
		Size: 136.6 MB (136562032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a56f34663d54cfb5c998cbdbc2d0f4ebff72ad6c3cf5b518fe3c29a23e0a2f9`  
		Last Modified: Sat, 15 Feb 2025 10:22:29 GMT  
		Size: 59.5 KB (59539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:062f6faf1e32123f71bf76b29001c4c71975742a12f74ec1643b6f4eb929b9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b0a0f2b18178c80d2d9d4b06a677e23d4e8a1f6cab6a91117b9cfbb935c69`

```dockerfile
```

-	Layers:
	-	`sha256:62b3f42a902b7a09922e85761aac37e285e187f9a348e8cda1a3aa4cf0ab6b88`  
		Last Modified: Sat, 15 Feb 2025 10:22:29 GMT  
		Size: 3.5 MB (3500662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b2bdc40441829bc9baa76c2404a34124458a89f27c34602cd25d771cca20e2`  
		Last Modified: Sat, 15 Feb 2025 10:22:29 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json
