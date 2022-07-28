## `gradle:jdk11-alpine`

```console
$ docker pull gradle@sha256:00848e72cd46c21ad67160e17bbf83efb481718ede07d15293eb8b9ac01b23b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:bd28db3b05a2572d2d886ff6b9a2b495982f1c498f0a2f3eaf2a8086ecb5f981
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365592967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110b668574a21eede93b2da0aeddd393faf3ad6321a25ee56fc911228829db90`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 28 Jul 2022 16:20:06 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 28 Jul 2022 16:20:06 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:20:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='32a93bd824cf34ccdde0881699a41a12722b4d8ff1d57294b2add2102432759b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:20:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:20:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:20:32 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 17:06:12 GMT
CMD ["gradle"]
# Thu, 28 Jul 2022 17:06:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 28 Jul 2022 17:06:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 28 Jul 2022 17:06:13 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 28 Jul 2022 17:06:13 GMT
WORKDIR /home/gradle
# Thu, 28 Jul 2022 17:06:17 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Thu, 28 Jul 2022 17:06:17 GMT
ENV GRADLE_VERSION=7.5
# Thu, 28 Jul 2022 17:06:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
# Thu, 28 Jul 2022 17:06:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2b3b9d0d1a1f972083dde62c850175d26be845971e3c96ff06c8145fbe2fd0`  
		Last Modified: Thu, 28 Jul 2022 16:25:19 GMT  
		Size: 12.1 MB (12050034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9875ccc97d0d48928ad5d42b8735e689578585611d1a6c20452e964c47b88a`  
		Last Modified: Thu, 28 Jul 2022 16:25:31 GMT  
		Size: 193.5 MB (193453364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9406868a12245358d162f9abe43d4aa81d7989b363b311962d858f0a01d5341b`  
		Last Modified: Thu, 28 Jul 2022 16:25:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa166bbf51b22e9bf4121ffc421e3f141240224bdde995d164b26ce70fd541f7`  
		Last Modified: Thu, 28 Jul 2022 17:12:05 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a26503862280fffd84e438fade65bdccd4e703bde5ff6a28752f195d6576489`  
		Last Modified: Thu, 28 Jul 2022 17:12:11 GMT  
		Size: 36.6 MB (36632924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2bb11fad112f26e69056fadc7f8b2f34f06618cc674e32f774eca582a1c481`  
		Last Modified: Thu, 28 Jul 2022 17:12:12 GMT  
		Size: 120.7 MB (120656347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
