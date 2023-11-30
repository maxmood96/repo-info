## `gradle:jdk21-alpine`

```console
$ docker pull gradle@sha256:334c5253bb53d4ef99562ff84fb29ad84d6619ebc524bf1f06d5a47ed497ff8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk21-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:dac99818870dd37e8143cff2cc5330304008fce04a90a3ef726d9dd33cd10c54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340908074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186aee3afc0a50c365a007594b5f5bb96d6fefd17278645c3eb3b3c85e12ed03`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 02:50:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Oct 2023 02:50:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 02:50:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:26:31 GMT
RUN set -eux;     apk add --no-cache         bash         fontconfig ttf-dejavu         java-cacerts         libretls zlib         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Mon, 30 Oct 2023 23:29:38 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Mon, 30 Oct 2023 23:29:47 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='77006c0a753808c2a6662007906eb6eb230f2fb6eb9d201a39cc46113e68f82c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|x86_64)          ESUM='422f23f5109056cacb9227247bebf8532e2dc3c9d505e71637ba610569d6b3ff';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 30 Oct 2023 23:29:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:29:49 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:29:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:29:49 GMT
CMD ["jshell"]
# Tue, 31 Oct 2023 05:23:53 GMT
CMD ["gradle"]
# Tue, 31 Oct 2023 05:23:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Oct 2023 05:23:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 31 Oct 2023 05:23:54 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Oct 2023 05:23:54 GMT
WORKDIR /home/gradle
# Tue, 31 Oct 2023 05:23:57 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Wed, 29 Nov 2023 23:46:46 GMT
ENV GRADLE_VERSION=8.5
# Wed, 29 Nov 2023 23:46:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Wed, 29 Nov 2023 23:46:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 29 Nov 2023 23:46:51 GMT
USER gradle
# Wed, 29 Nov 2023 23:46:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 29 Nov 2023 23:46:53 GMT
USER root
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3c4df72d74e9b84f1215596adc1b562a87b2c2bd9249ba1433455079b00218`  
		Last Modified: Mon, 30 Oct 2023 23:35:19 GMT  
		Size: 13.1 MB (13141022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557d0e6d84070f1613c688db633bc297fea0a029d3a22d4fe738533f232c1d43`  
		Last Modified: Mon, 30 Oct 2023 23:38:41 GMT  
		Size: 157.7 MB (157664989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b015da0bc5f29d7e54638ef2c9b6621d293e70c697f7a84d606b0c468ad4bbb9`  
		Last Modified: Mon, 30 Oct 2023 23:38:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae9403a54ca68efac5723aeaa16e4f4fb7045e4d0fa413ee823194acd675092`  
		Last Modified: Mon, 30 Oct 2023 23:38:29 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24701d8c6808fa0719633d33e237e49635bf4633f0e489af27829b309db7b963`  
		Last Modified: Tue, 31 Oct 2023 05:32:12 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37771cc229f22e0d12ac4019f895a596fd2364dc870ec991b9fc44cd3d4123a`  
		Last Modified: Tue, 31 Oct 2023 05:32:17 GMT  
		Size: 34.2 MB (34153239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072273a68ddbc47e7e75d367bd2a384bcb9f93ac2c75f2267a6b0caae2d90c70`  
		Last Modified: Wed, 29 Nov 2023 23:55:05 GMT  
		Size: 132.5 MB (132544450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720a56b9e0afc833e5f5aa4456dc373e55539c5fb77bfe4358bb9efd902382b4`  
		Last Modified: Wed, 29 Nov 2023 23:55:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
