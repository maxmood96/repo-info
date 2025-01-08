## `gradle:8-jdk-21-and-23-alpine`

```console
$ docker pull gradle@sha256:523c471bdc3e56eac341735cf4714f80ee0e0d121b41eedb672c9022ff338048
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-21-and-23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:ae78ad491a2873f34320164df49eb1e2ec607dc11f35267d2e3b5551ca765df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.1 MB (515101020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5f7ccdd5d516f52433c5770d56a57e73ee885310308a225dfc2c395a2e6541`
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
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 20 Dec 2024 17:54:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
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
	-	`sha256:74124278afe2b18a31c86c5481b70f13610d72f9251456efb60077c008ba80d9`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 20.6 MB (20646874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8fcf39531b5efa8fb9a8f692b5b7b7feca498796d140b94c6255523f4c7f6d`  
		Last Modified: Tue, 07 Jan 2025 03:31:27 GMT  
		Size: 157.8 MB (157779528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62fe376e35d90e3e99f049badca94e8fe7301d699d6a2539330a8994d9f8799`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5d46d44a8796aecf2575f05400a60dd8d65d4f9f801590d09cd3b4f278318d`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb2948816ca5538d2f1a417f1e9f2537081fd0b1b86269d4ec5f9f71080942`  
		Last Modified: Tue, 07 Jan 2025 04:20:25 GMT  
		Size: 165.5 MB (165513333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88753da3702a1eebf15024bcd2b77c150d80ec9c1f723a78c4e26690528f61e9`  
		Last Modified: Tue, 07 Jan 2025 04:20:23 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4236fb07c375b7c18ec479455597d02c05d5a31d9f293e70b39628ec8cb88ec`  
		Last Modified: Tue, 07 Jan 2025 04:20:23 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0a0e49240d90cc4f17bf1f5d913dd5f9ae6ba571832f07caca7b6f6d8b8cf9`  
		Last Modified: Tue, 07 Jan 2025 04:20:24 GMT  
		Size: 30.9 MB (30924484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccc41d91493abeff70a5fd0ebd97bb916c64384efd318b8ba22f43a62896a74`  
		Last Modified: Tue, 07 Jan 2025 04:20:26 GMT  
		Size: 136.6 MB (136564171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ccc697f7958156c37e77c24c34457d58a14e89a7b433af5d145252ab92ddd8`  
		Last Modified: Tue, 07 Jan 2025 04:20:24 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:d5f9fcc0354fe5a3641bb5016f3789cc29e778710845d3e4c0153c7deee959c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221d98b468d32bd96ce8c9a5c08fca6763c4b3a794a47c8e4d29c314e2f0d285`

```dockerfile
```

-	Layers:
	-	`sha256:0b44ccfba84171b188c49401f9f959cae8531b370b250d8cb530ca51a5a67b1a`  
		Last Modified: Tue, 07 Jan 2025 04:20:23 GMT  
		Size: 3.5 MB (3462341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269d6eeebaa192599521ba152c16d6977cccb0d69be30cdaeeb513c6a9d0d90d`  
		Last Modified: Tue, 07 Jan 2025 04:20:23 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:94c88284d94432e6b34d17e5e7b04c21e2edcfdb8706c7cda158e5fa47b4ab24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.7 MB (511710206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1529916fde5174fc2f237323a067a7d78b4578674eadf784d35cebbf0f575ae7`
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
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 20 Dec 2024 17:54:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
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
	-	`sha256:cc7e26f108db4058af6f9154e47e87b732fbd6fb04792a0871d1074952992b75`  
		Last Modified: Tue, 07 Jan 2025 07:27:36 GMT  
		Size: 155.7 MB (155740151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3ed595529c90be877f0b53e3b866c077cd55bd6b85c36388f452338ba4c676`  
		Last Modified: Tue, 07 Jan 2025 07:27:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3a0beda2910401756d0ac146e871cdae993a2a999f118127df9ca88c508fc0`  
		Last Modified: Tue, 07 Jan 2025 07:27:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bdf1e8bc30716c4cb1a99078d875527ed2cc22bb1b7ae471135fc1400cfb64`  
		Last Modified: Tue, 07 Jan 2025 16:30:48 GMT  
		Size: 163.3 MB (163316110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f2487f7a0e85221a9e73253388e2f266b5181bd34743995a1637349ea54e0`  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0d350a7794110508d679d122fd4a72acc4f3afd6a38927a5139931ea3835ea`  
		Last Modified: Tue, 07 Jan 2025 16:30:22 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566b7dd7873aa80ec0fd192c32c3d210d491977e0e4a9c57b6c0dff9b9e997e1`  
		Last Modified: Tue, 07 Jan 2025 16:30:24 GMT  
		Size: 30.9 MB (30906386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a2576867d0da88f272b7e6c4f6c4db4b089738f0107508165a8e823170e1e`  
		Last Modified: Tue, 07 Jan 2025 16:30:27 GMT  
		Size: 136.6 MB (136564248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa50693e7ea00eca7921e976a54868ac051b7ec0ea5b00c77340df97de1b47b`  
		Last Modified: Tue, 07 Jan 2025 16:30:23 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e8ab00d072d3348dd027b1b22d7760d124a90137d25b737400d9c6962c80a8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c654d1433129b11ad9bbd13a3b96422dce89930d01378d666e7974f5384f1e`

```dockerfile
```

-	Layers:
	-	`sha256:fd1cf90bf67f619c596fab3f292ae029cd3e8e17d047160c6dd6b9e03723f416`  
		Last Modified: Tue, 07 Jan 2025 16:30:23 GMT  
		Size: 3.6 MB (3565773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7bd43dcf1b180ce48bcea3f4e8b9889ad543b202604b859949fd2e7ab661608`  
		Last Modified: Tue, 07 Jan 2025 16:30:22 GMT  
		Size: 30.9 KB (30934 bytes)  
		MIME: application/vnd.in-toto+json
