## `gradle:7-jdk-alpine`

```console
$ docker pull gradle@sha256:f3d11c84b2c5bb6e55c2e9549a47712a3f90c9a7ae7e6f4825e0a30d2634d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:7-jdk-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:6c46aaec63705dc3e30875ec1f2c6e367c1b17d3df4bdf3490d606d0ac454a64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346434940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d95ba6d9e68964758b936d11eccd2ff7ed1f8a0fc342c3a3f90c3808221e2d1`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:09:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Mar 2022 06:09:17 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Tue, 29 Mar 2022 06:10:54 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Tue, 29 Mar 2022 06:11:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a07cc09db0e71d06ea388902f8fcea8151b2b9ba51a16f75f9c0a3ac9acbfb61';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 29 Mar 2022 06:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 06:11:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 29 Mar 2022 06:11:18 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 13:28:48 GMT
CMD ["gradle"]
# Wed, 30 Mar 2022 13:28:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 30 Mar 2022 13:28:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 30 Mar 2022 13:28:49 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 30 Mar 2022 13:28:49 GMT
WORKDIR /home/gradle
# Wed, 30 Mar 2022 13:28:53 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Wed, 30 Mar 2022 13:28:53 GMT
ENV GRADLE_VERSION=7.4.1
# Wed, 30 Mar 2022 13:28:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
# Wed, 30 Mar 2022 13:28:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8b72f2e4b8ed4ba22286a50d6f2bf2b7f79589f32f8c9de1f0e643014314af`  
		Last Modified: Tue, 29 Mar 2022 06:12:48 GMT  
		Size: 430.5 KB (430474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e13044408dddd883519d3c3f4362ee5a4a3e5a9ca7312d35240762d620aeda4`  
		Last Modified: Tue, 29 Mar 2022 06:14:53 GMT  
		Size: 191.9 MB (191924789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68db792a8b376baf4ed9fc089950287c8a1c1426b31dc303e47cd841a3c26c4f`  
		Last Modified: Tue, 29 Mar 2022 06:14:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36b13aca76f1c99bb70b6fe41e7cc997977447fcfbc8fdcb72ccc30d6b8000e`  
		Last Modified: Wed, 30 Mar 2022 13:30:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cab42ac787c6973330d74a2f2fe1b27216c217d03c09a6b94ee31f8085e3c1`  
		Last Modified: Wed, 30 Mar 2022 13:30:59 GMT  
		Size: 35.4 MB (35398456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca35390dafecdee1fc279f21ff74be6ec0e89004904bf341a0da8ebc7d25a0`  
		Last Modified: Wed, 30 Mar 2022 13:31:00 GMT  
		Size: 115.9 MB (115865222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
