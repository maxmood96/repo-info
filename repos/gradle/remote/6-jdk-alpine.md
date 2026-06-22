## `gradle:6-jdk-alpine`

```console
$ docker pull gradle@sha256:e98dc1503f0533d04e2bb1854c2371a4249842c663e3cd8efe67c1d987c4cd9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-jdk-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:092ceea8dcefe9389b7ae4a3232b7b623dbcca60d549ba51bbedcffc73307190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314444472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a12871ebb45c9d55dd1d661f1c65c7c2e7d829f6fd2f70543ad1d1bb97c1f1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 22 Jun 2026 19:56:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:43 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:19:36 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 20:19:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 20:19:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 20:19:36 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 20:19:36 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 20:19:38 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 20:19:38 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 22 Jun 2026 20:19:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 22 Jun 2026 20:19:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 20:19:40 GMT
USER gradle
# Mon, 22 Jun 2026 20:19:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 22 Jun 2026 20:19:41 GMT
USER root
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9b522ef6226b5e762f07b84e312e749c4ff9762d64fb0a0e6a0f08d3dadc9`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 16.8 MB (16815695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82edf31c58962a79b82269852db50864e5e46165fd344f4918a80796db584951`  
		Last Modified: Mon, 22 Jun 2026 19:57:00 GMT  
		Size: 141.1 MB (141074581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6857b309472f9776411dbc577858d377ec37fa81f85b3d973ce4c495a1a72e`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2ca25c879ff73f76024b21ff3fcdcae040cc01923ae1d2bf184bd72f35d3bf`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb06f7ddbc11149cd2ec4dafe5d13d22e2ce11016df072bd86ec4e7558e3d5`  
		Last Modified: Mon, 22 Jun 2026 20:19:55 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9e3d9dbc589885ffb2697a4d3fd22df089f4e4cb59ff0248ba89daccd18599`  
		Last Modified: Mon, 22 Jun 2026 20:19:57 GMT  
		Size: 44.6 MB (44578420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c3f4e5371b7b29d3e05ce78e8eb7f57a7c20b72fb507a62ccb37f1fe89791e`  
		Last Modified: Mon, 22 Jun 2026 20:19:59 GMT  
		Size: 107.7 MB (107696630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce4080303392795ab85557c2fcdbb7c81b875d8ef980a7fb2a3becce2f9195f`  
		Last Modified: Mon, 22 Jun 2026 20:19:55 GMT  
		Size: 431.3 KB (431272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:57c7f425ae23649eaf046ab0fca31449e55f12387e8c9b75719347b7a50729ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4501737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3119d524e658caf68195ef964375b3f76c6bef18bf93d918d530d49a04dce545`

```dockerfile
```

-	Layers:
	-	`sha256:b9ac8cd8b924bf1db3f821d089097e2ef942b22d8031da349319270dfc18b35f`  
		Last Modified: Mon, 22 Jun 2026 20:19:55 GMT  
		Size: 4.5 MB (4477731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6541998ce7ee8cdb841954587dafbe8edfa04963ec4d5dfb43f6c5b7c42803`  
		Last Modified: Mon, 22 Jun 2026 20:19:54 GMT  
		Size: 24.0 KB (24006 bytes)  
		MIME: application/vnd.in-toto+json
