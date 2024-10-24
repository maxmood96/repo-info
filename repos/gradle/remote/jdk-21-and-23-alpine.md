## `gradle:jdk-21-and-23-alpine`

```console
$ docker pull gradle@sha256:39cb094e0109627357f95cc530185b62d1ad146b5b604f20f09ecf0c21a4d354
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:dd64d0a4960a0c6396ae78fc48d9dfcef170ea6f4823e3c53b880e20b9d1406a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.5 MB (517503593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08c342d15259b42be9d36dc287d6f2c172f9b0f06728956f0d0257e3bab9a72`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Oct 2024 03:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 03:51:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Oct 2024 03:51:19 GMT
CMD ["jshell"]
# Wed, 16 Oct 2024 03:51:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Wed, 16 Oct 2024 03:51:19 GMT
CMD ["gradle"]
# Wed, 16 Oct 2024 03:51:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 16 Oct 2024 03:51:19 GMT
WORKDIR /home/gradle
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 16 Oct 2024 03:51:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 16 Oct 2024 03:51:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
USER gradle
# Wed, 16 Oct 2024 03:51:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
USER root
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d261c61120750cb19b5bf351e17be8ac00173617f566054bdbd38eec29dffee7`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 23.0 MB (22953305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7043234fe874c842910e4944da3626930f5c7cc4dbd29b50f6a4f907a7d8feaf`  
		Last Modified: Thu, 24 Oct 2024 00:57:11 GMT  
		Size: 157.8 MB (157779374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859106f999588717f76b6609fe5d34f5d2c2fd62e7edbe86c9a8709b1954ba5`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc23d54cb8e8eb85a2d0b34c310691777d93c7b037f48f9063d4eb2bb338ee6`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b9de81b0e40ff987cd9d3fc2eb62cf3140e925a820a66121bb5a8c889f3c37`  
		Last Modified: Thu, 24 Oct 2024 01:55:37 GMT  
		Size: 165.5 MB (165513424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071e7b54116c0741432eb5bba11b4b1721571636429042bddb127b91a87f1e9f`  
		Last Modified: Thu, 24 Oct 2024 01:55:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90032afa2fc258cbaedfc8d2c983d2207cf2dfd898cd20d57834332a429b5020`  
		Last Modified: Thu, 24 Oct 2024 01:55:32 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca7a948eb3f62f4626d7da2851dc1f1ee59fcd9459196b290ada1ff7baf0313`  
		Last Modified: Thu, 24 Oct 2024 01:55:33 GMT  
		Size: 30.9 MB (30899415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053553975bbfa57d7e8fbd00b8e78036aed7d669a321b9c26b65ba66161d4a4`  
		Last Modified: Thu, 24 Oct 2024 01:55:37 GMT  
		Size: 136.7 MB (136730234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605f8c8a18e4a7076360bee85ad91a9f370ae3819f61399b4ce661f70bc8c8a8`  
		Last Modified: Thu, 24 Oct 2024 01:55:33 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:576c9f0b3024124e7f6bd81a537b301c3fbcd1ead9063a0b004d21eea6836335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396b77a73c5e5cd790de3dc3735367bcbce147ad460899be35a7b4fd9789bf81`

```dockerfile
```

-	Layers:
	-	`sha256:363ac4703c6ee0748f91f75429a0c5418ec05fcd089720ddbc559440377e7a44`  
		Last Modified: Thu, 24 Oct 2024 01:55:32 GMT  
		Size: 3.5 MB (3467880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d88b78129dfe586e1f8b85f8f9568dc16a1f58bcc765a59cbf6233dd8312cc`  
		Last Modified: Thu, 24 Oct 2024 01:55:32 GMT  
		Size: 30.7 KB (30702 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:76328645220beea2e02b4098691b57e5a41f54456071b636431ca27e736d533d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.5 MB (514492814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e131699776a1da336d9e6b8a266217db7bf092e8062f81e34a86b9188fac790`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Oct 2024 03:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 03:51:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Oct 2024 03:51:19 GMT
CMD ["jshell"]
# Wed, 16 Oct 2024 03:51:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Wed, 16 Oct 2024 03:51:19 GMT
CMD ["gradle"]
# Wed, 16 Oct 2024 03:51:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 16 Oct 2024 03:51:19 GMT
WORKDIR /home/gradle
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 16 Oct 2024 03:51:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 16 Oct 2024 03:51:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
USER gradle
# Wed, 16 Oct 2024 03:51:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
USER root
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5ab350b8ff57c75640d387c970dd2282464d9836a98c0f02d04ffe85d3db64`  
		Last Modified: Thu, 24 Oct 2024 01:14:18 GMT  
		Size: 23.7 MB (23731419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106ebdb43fd997ba88f0aac72b687792bf1eb78b471f3d80833b2478939280e5`  
		Last Modified: Thu, 24 Oct 2024 01:14:24 GMT  
		Size: 155.7 MB (155740142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880307f28a09156aa3f74cc0ead3743e36be7611be3e05201b44d035d0c53a8e`  
		Last Modified: Thu, 24 Oct 2024 01:14:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285861aa94b115f54d51eac6aa0cbba4672c4604eb4591b88d706a5874cfdb61`  
		Last Modified: Thu, 24 Oct 2024 01:14:17 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445af85755ce6ce096e6ab3e135106f8f3802ad92fe8acdb4a6552f47dbab11d`  
		Last Modified: Thu, 24 Oct 2024 02:43:06 GMT  
		Size: 163.3 MB (163316178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24840fe4cf0a74c3fac0bd5e2018eba07ddc1dede4aa0da05378822a7864a666`  
		Last Modified: Thu, 24 Oct 2024 02:43:02 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df88cd11e4e1fcd4a880f298ca4184abc36023ccc224e544d8e7403408f59d8`  
		Last Modified: Thu, 24 Oct 2024 02:43:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efeee3240a2a5220adbd665050da5d8400817d66f8b581133aa4b30afaf7739`  
		Last Modified: Thu, 24 Oct 2024 02:43:04 GMT  
		Size: 30.9 MB (30883058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322b194b7db21ed28c4760c8399b20163399246d92b7f770e46edae20019d14`  
		Last Modified: Thu, 24 Oct 2024 02:43:07 GMT  
		Size: 136.7 MB (136730338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0941a8338807ce46375627c456e185f380229e3ca8fae8fd46ec24091f549176`  
		Last Modified: Thu, 24 Oct 2024 02:43:03 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:016c8ea9bfde651570fdbbedb13b4718a81e43719fceeb114d365ee163e0e4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836fa2cde5e966ddad60ae152f0c6adeee16563cb42c614aebc1f6a86f4d54d`

```dockerfile
```

-	Layers:
	-	`sha256:34e947ccbdefe260066b6b3e899d717952b6c4b44c76505bf357988b29a390f7`  
		Last Modified: Thu, 24 Oct 2024 02:43:03 GMT  
		Size: 3.6 MB (3571471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83360917eb9694cb775477ea7adc0ebf512abc4615ce125f66a4fcf037d5692d`  
		Last Modified: Thu, 24 Oct 2024 02:43:02 GMT  
		Size: 31.0 KB (30994 bytes)  
		MIME: application/vnd.in-toto+json
