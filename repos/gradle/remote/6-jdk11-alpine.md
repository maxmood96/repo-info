## `gradle:6-jdk11-alpine`

```console
$ docker pull gradle@sha256:4b0e36fcf13474434f32cbbc5ca8bf72d17310e924c23f54d31e35e57bc1debc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:db57eea858084d9d5cd3b1a693ac516401848ffbd0ceec5e2659ad79bbed9b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.8 MB (302773676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aea31bf25ce7c9173d750f236975d42853160d0248b5d9ae4d7b6bb0cf47b70`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e1f667395cdb1e872bd7320e3eda96c0f0978e29e574e75f9cdf61160e8974a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["jshell"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bd9bbffc5734efb01844a29a113ded889f4da3cda8e182581f06df7d1b2166`  
		Last Modified: Fri, 14 Feb 2025 20:34:24 GMT  
		Size: 16.2 MB (16175556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886f759d872db74834cddc7f5de5e1d9dac42f43af6818800b460c7c7f23fdf`  
		Last Modified: Fri, 14 Feb 2025 20:34:35 GMT  
		Size: 140.8 MB (140769675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87b59c7b26a9d55a851b5445f42627ca08826874def4fe66efc11b30e2a73bc`  
		Last Modified: Fri, 14 Feb 2025 20:34:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0963aeeacb77ac39d9fdb8e3dbd9693ba930911be387409258faf61e0dc202fb`  
		Last Modified: Fri, 14 Feb 2025 20:34:09 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe850fff04e725478a7c09c169d3c675493c379c2d9ad4efbc9e688cbdede99`  
		Last Modified: Sat, 15 Feb 2025 00:23:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121a501967a24f65dc028760714de0fa032890ce766612d21479a82def200388`  
		Last Modified: Sat, 15 Feb 2025 00:52:02 GMT  
		Size: 34.1 MB (34054705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b53b2397c899e73ed2301a76ff01cff476ca70be7fa2d6bd1647766b3c32b`  
		Last Modified: Sat, 15 Feb 2025 00:52:05 GMT  
		Size: 107.7 MB (107696766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6563214074880638a1ef023a6d21751d462583339e91d4d4713a730384d0f32c`  
		Last Modified: Sat, 15 Feb 2025 00:52:03 GMT  
		Size: 431.3 KB (431278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:b0d382e4e9d11bde168f2eec255569db7725c77204953e236c3571c47ec64e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d189dc40ec75e04503b7d7bb1ade52b8070fd61f9e34a8c08413d0cfbf4a3ec`

```dockerfile
```

-	Layers:
	-	`sha256:46ebd4615a92d544db2d2bcd8bfb4e95dce2e284fdf5dd7f99963a0dfe4a903d`  
		Last Modified: Sat, 15 Feb 2025 00:17:27 GMT  
		Size: 3.2 MB (3153812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e01a67522176d97de19dd51fe8e973f8064ad886f568e4a1583bb477985d26`  
		Last Modified: Sat, 15 Feb 2025 00:17:27 GMT  
		Size: 20.6 KB (20601 bytes)  
		MIME: application/vnd.in-toto+json
