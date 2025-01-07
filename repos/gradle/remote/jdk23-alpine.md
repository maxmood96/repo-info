## `gradle:jdk23-alpine`

```console
$ docker pull gradle@sha256:843c14ce11ae592ab707764093265c82fbb7adf255cefc99dbed6d58d4b1e3db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:22c77678c12563746a5adc95e65f0eb1539a71a6a98631f1ce33be0c3b9211f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357321035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55d0ed090935bf2f059d4a139048e3a1fa4eb0fe0675068f80e49dee8ec0b55`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER gradle
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER root
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225cb0f2398c82803e0a664bca2838b6952c8625269bacb10309a51d08b246a7`  
		Last Modified: Tue, 07 Jan 2025 03:31:55 GMT  
		Size: 20.6 MB (20646818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372a9834e30bc1a4ac9cf9ed49635b1495df06f03aec898ef29d50dabefc1db`  
		Last Modified: Tue, 07 Jan 2025 03:31:58 GMT  
		Size: 165.5 MB (165513260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9c3a812f9de067e26e45678b86e96db89e7f0dae9089fbdc3c188e4238f4f1`  
		Last Modified: Tue, 07 Jan 2025 03:31:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec9ff0efbdd4303d78867776fe04d39637d68c10fe145cb24df20fc8b1f2478`  
		Last Modified: Tue, 07 Jan 2025 03:31:55 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460fe526103d97fd9c64134578fef63d67dc6aab4aa9b43ab1814598e0993237`  
		Last Modified: Tue, 07 Jan 2025 04:20:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd4fd1958da9cbc535052974134e737a2af4d9d6f8ae33f96ab24ebf397e1ab`  
		Last Modified: Tue, 07 Jan 2025 04:20:12 GMT  
		Size: 30.9 MB (30924422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f92a20a8c9e889ab11bab535761adb422ba7b81a7834b510f04d889f60f4f8`  
		Last Modified: Tue, 07 Jan 2025 04:20:13 GMT  
		Size: 136.6 MB (136564174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459245c1a52d8476ce8aa0f452cc81dd1f3b0cf2c2a5fb211d1f9ee8e4f88d34`  
		Last Modified: Tue, 07 Jan 2025 04:20:11 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:d9a648fd50f83e6e7c6a84bd3b9ffb97974b8708771d12a8a44234c9d3a58cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b23cb21e6730c915eeaf4d5ad84d30f82d5d33d366fe5817f53dbc002bf782`

```dockerfile
```

-	Layers:
	-	`sha256:184c3a39eab88d04d65905518e9b5f92ba9ddf1ea44814945695d7e4df646afb`  
		Last Modified: Tue, 07 Jan 2025 04:20:11 GMT  
		Size: 3.3 MB (3305862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02d32e5b1012cf50528debfae69df3e045ef635982b99796d13232b6f335bbb9`  
		Last Modified: Tue, 07 Jan 2025 04:20:11 GMT  
		Size: 20.9 KB (20912 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d210ce9218ebaad2a8a41e7df4cfd910cc1e4eef06fa792a42517f1eb94058d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (355969637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6808dc16e4f42f2963b21f5ef6c423b066f4400aedddcbabc3552a43f61441b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER gradle
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER root
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0debfbcf140de1b1e0c5b7204c63e292d79de69a68e3267957c67e04f0ba24af`  
		Last Modified: Tue, 07 Jan 2025 07:27:36 GMT  
		Size: 21.0 MB (21033362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271c5440a9be225779e8c897625e08ef3a668a433a36b7f76f003525d28a90b4`  
		Last Modified: Tue, 07 Jan 2025 07:28:54 GMT  
		Size: 163.3 MB (163315901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2451b325c4216d4a90edcb536b5e9fb94cc834cee8db6ff07edf76e0e8ff6a41`  
		Last Modified: Tue, 07 Jan 2025 07:28:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89668996c2dc517311f1cd835fb76d89cb2e42ce58232c8f1a8a9544f33d9b63`  
		Last Modified: Tue, 07 Jan 2025 07:28:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d10de88f27a4e4f3c92e22210e5b2eb536416a74a0b8bafaebd92cdb525d38b`  
		Last Modified: Tue, 07 Jan 2025 16:29:34 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cd000c932cc16abd8f01df92436753530d4e72227aeb5ecabfc22375f7733d`  
		Last Modified: Tue, 07 Jan 2025 16:29:35 GMT  
		Size: 30.9 MB (30906438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd78e1baa83d041f59e09ba7415f861873e2e03cabad202e3e55e18a4f347ebe`  
		Last Modified: Tue, 07 Jan 2025 16:29:37 GMT  
		Size: 136.6 MB (136564251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6efb55388ae6b95c187861b4cd4d6d3f169accda99c78828182eee3413d5b8`  
		Last Modified: Tue, 07 Jan 2025 16:29:34 GMT  
		Size: 59.5 KB (59538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:44410e8b6e7be3599744207af7451366f4c5da9f126eeb3f7dee49bcf92bbd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5cd7ecee0d4eb70d0e17f6420b9c6ab5587243b81dd35c18f21a6f352336a2`

```dockerfile
```

-	Layers:
	-	`sha256:28fcc9a273e74d48624092cab5ecb812ea8d32dc560c9a007d20d50c7307ff0b`  
		Last Modified: Tue, 07 Jan 2025 16:29:34 GMT  
		Size: 3.4 MB (3409868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3097a921aae4370898b109c82b676889a463cb61b0ad9f479239722c685e6cdc`  
		Last Modified: Tue, 07 Jan 2025 16:29:34 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json
