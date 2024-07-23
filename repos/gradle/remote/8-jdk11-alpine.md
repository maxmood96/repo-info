## `gradle:8-jdk11-alpine`

```console
$ docker pull gradle@sha256:e0c65a0a5e278d0298dd775a29d01eadfd7919572af443ae1596d9130d70361f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:8-jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:0a70c54a20155e465e49680bbab25c4b4cdf841865311df22acdfc14fbccf091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324665623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34880ecde07aedd820faa3398b6ef0ccf36095a72dbe2dfba295bb8eaf1de345`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b45c467be52fe11ffd9bf69b3a035068134b305053874de4f3b3c5e5e1419659';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:f52f359cd8d0e18fe23ad96c88a4ed275ce3c28c031f134b2223544d799cb126`  
		Last Modified: Tue, 23 Jul 2024 01:05:20 GMT  
		Size: 8.5 MB (8537043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87267a151054e11857fb24bf9e6346353ea09cebe4ed3ed139eb18460fe0c4`  
		Last Modified: Tue, 23 Jul 2024 01:06:04 GMT  
		Size: 140.7 MB (140686030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f874197a9f80451cacd73e17573fd76276f089d329bb564115fbc0f2c830d1d1`  
		Last Modified: Tue, 23 Jul 2024 01:05:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb836745c0f2669509f78a387d020a86cfca8379fb4ef0f3136942bd882edd`  
		Last Modified: Tue, 23 Jul 2024 01:05:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598a934d24381efc240ff9f4473ca28420cfe4fba2c1831be70dface8641b559`  
		Last Modified: Tue, 23 Jul 2024 02:01:07 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba0f253cc74c07fe5973d857d1097224c3b2d010486cf1753afec155a0285d`  
		Last Modified: Tue, 23 Jul 2024 02:01:08 GMT  
		Size: 35.9 MB (35889066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa98026317611917b0cffd87eb2dd81003b4a0c45f83ac4261ed5c1a1af35b0`  
		Last Modified: Tue, 23 Jul 2024 02:01:09 GMT  
		Size: 136.1 MB (136131941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0b073cb218ed17db1cf9c2a2fca09eba89ea5196c04e411e46f9e2cdc7e7ff`  
		Last Modified: Tue, 23 Jul 2024 02:01:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:87e8f858d00a35fd0aa819179f89bd707cf3c44e001e7bb16f75fa7facbbbc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3413181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370dd74d56cd4f7b35065fbb291d02b485137a975aae119cdbe72d1a09ee88e8`

```dockerfile
```

-	Layers:
	-	`sha256:729f37a3396259de606a945b9bf3f3f5fb9e7e29e96dcc88529d5e56372d3609`  
		Last Modified: Tue, 23 Jul 2024 02:01:07 GMT  
		Size: 3.4 MB (3392318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:932ed97c91c6c5bc4b88d97902d27d642c940fa323b424c83406bbf16f0e0aa2`  
		Last Modified: Tue, 23 Jul 2024 02:01:07 GMT  
		Size: 20.9 KB (20863 bytes)  
		MIME: application/vnd.in-toto+json
