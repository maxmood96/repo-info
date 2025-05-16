## `gradle:6-alpine`

```console
$ docker pull gradle@sha256:21507dcdd8b83b9824dc7c22a3480a07ef1bfe5613808ab40c43a1b6876b5cc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:f07a4bd385a7fcee97916618251fed78b242f871268c289ad92cfeb3c7f5781f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.8 MB (302827973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3146c780125e0fb2f164e43b241584e7f940358ad1ed0ddc70d19e60b4534`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5defac0a735690b04bc1bbe9d7e3b5faed6dd54f946858349ba114394f8fb386';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fb80b85f2e06395a680c151acc346eace748772c5dfcc2fd50b2ae7716c056`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 16.2 MB (16176494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bfe6213f13619e9e9ebbe87b75aaa8f626fd50f8b08cf9cb9a10d5c483f13`  
		Last Modified: Thu, 08 May 2025 17:05:19 GMT  
		Size: 140.8 MB (140800007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c584005aa0ebcfc3f44fdf621ebc001e2708a1311f8983bc1a2f01757e8f66f3`  
		Last Modified: Thu, 08 May 2025 17:05:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6326336b8bc46943e00b2c52f2bac37c63402a67f96ede207c1fbc403b0859`  
		Last Modified: Thu, 08 May 2025 17:05:20 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d380b9a32d78d81b8a073411db442b774b0732a5588fd980736c591d7d695e86`  
		Last Modified: Thu, 08 May 2025 17:56:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eaaa55f2ed1198481aa4fd21d8d30075dde439aea705e4b83e33d6917ee426`  
		Last Modified: Thu, 08 May 2025 17:56:26 GMT  
		Size: 34.1 MB (34077798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8814709f6450f7b1206b1ce3945307ed913125446a3ce6f9295af78547e8468`  
		Last Modified: Thu, 08 May 2025 17:56:28 GMT  
		Size: 107.7 MB (107696704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b038029e2c3febf9c6dad48a985ac3d01df5a6b68c249809e535b7bc9a7cea5`  
		Last Modified: Thu, 08 May 2025 17:56:24 GMT  
		Size: 431.3 KB (431272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e319656ccba95e57595df42a8520617864270998910f6528a7137b0d12d91985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab9641d31cb4634eb4defe4ddab699d48314a6d51d903fcc3b7be5e772cce73`

```dockerfile
```

-	Layers:
	-	`sha256:3ef18b3df689a26781445cca3584ccfd4c9c0e31b8c2bf6e40ca8fc47a20b992`  
		Last Modified: Wed, 23 Apr 2025 17:10:30 GMT  
		Size: 3.2 MB (3155532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd9e50f024bd7a4d2651ff031460b706d5c4f5f285999b333af3029c792a85d`  
		Last Modified: Wed, 23 Apr 2025 17:10:30 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json
