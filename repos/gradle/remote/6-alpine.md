## `gradle:6-alpine`

```console
$ docker pull gradle@sha256:d588837c8f6eab947f4989e1a33aee84f894aaa6e047350b6a55aa3a1628276b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:3d2ec9d5c040e8d04ab3ec9afac2714596c15ed2d249025b8da38c865467edad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61eff9005ef304245c42a52cd64ae3ebb7d98268a6801dc3605a47f564483e87`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5defac0a735690b04bc1bbe9d7e3b5faed6dd54f946858349ba114394f8fb386';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 29 May 2025 19:34:11 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:34:11 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 29 May 2025 19:34:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER gradle
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER root
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fb80b85f2e06395a680c151acc346eace748772c5dfcc2fd50b2ae7716c056`  
		Last Modified: Wed, 23 Apr 2025 16:31:34 GMT  
		Size: 16.2 MB (16176494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bfe6213f13619e9e9ebbe87b75aaa8f626fd50f8b08cf9cb9a10d5c483f13`  
		Last Modified: Wed, 23 Apr 2025 16:31:36 GMT  
		Size: 140.8 MB (140800007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c584005aa0ebcfc3f44fdf621ebc001e2708a1311f8983bc1a2f01757e8f66f3`  
		Last Modified: Wed, 23 Apr 2025 16:31:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6326336b8bc46943e00b2c52f2bac37c63402a67f96ede207c1fbc403b0859`  
		Last Modified: Wed, 23 Apr 2025 16:31:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ae9d3ae31073ef1b00357d54bed084a48af59316614cede6c322f264b5e422`  
		Last Modified: Mon, 02 Jun 2025 16:48:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7122df4c7f0d353e6714517e5f542d3e75fe03204a9650c84bb2930470d2ba69`  
		Last Modified: Mon, 02 Jun 2025 16:48:28 GMT  
		Size: 42.7 MB (42725790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e682ec89d0290adff81b2513b0007a6f5a7a38e4bc3b94d49bfbd36d0caa26`  
		Last Modified: Mon, 02 Jun 2025 16:48:29 GMT  
		Size: 107.7 MB (107696747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90faa9f125e1a155204ed002a8455dab30cad38901ae7b0957f5d103d6aa8d`  
		Last Modified: Mon, 02 Jun 2025 16:48:28 GMT  
		Size: 431.3 KB (431276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:11f2075e6c5ce80e5171cb7b078ca4c7f5bb47d2e53c40cdd7e5cafcc7b11164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4545800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2433aacbaeb92b9b4635863b9fda359f5c091ee9abb2439a70ea00d3b434d2bb`

```dockerfile
```

-	Layers:
	-	`sha256:e8815f9791efd33f26db8bc1341c2710f221b5b9f147a6f9c8a924924285e77b`  
		Last Modified: Mon, 02 Jun 2025 16:48:28 GMT  
		Size: 4.5 MB (4521738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca558956844014569b973e74dc7142fe0bd9f0e1f2670ef5c969bf9a2c6fca7`  
		Last Modified: Mon, 02 Jun 2025 16:48:28 GMT  
		Size: 24.1 KB (24062 bytes)  
		MIME: application/vnd.in-toto+json
