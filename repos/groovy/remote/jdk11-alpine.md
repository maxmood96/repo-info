## `groovy:jdk11-alpine`

```console
$ docker pull groovy@sha256:0f0a4541446bd309ff1b739c4567ee12746e72a3eaf92a6f7c2e407df330226f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `groovy:jdk11-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:1eebdfe38dd9798fdaf07f9ee8c20764103920892f019cb89c7b5cb2822e3e1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240333617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5bc85040152bbb80142a93f0528a3861c122e9ecb557e2a57996f3c090d75d`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Thu, 13 Jan 2022 17:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Jan 2022 17:19:46 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Mon, 07 Mar 2022 19:26:29 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Mon, 07 Mar 2022 19:26:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='99e13a167ac27fac3dbfcc394a024fd9f4d84d24734ad5c250f97215d496ee36';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 19:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 19:26:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Mar 2022 19:26:56 GMT
CMD ["jshell"]
# Mon, 07 Mar 2022 21:03:32 GMT
CMD ["groovysh"]
# Mon, 07 Mar 2022 21:03:32 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 07 Mar 2022 21:03:33 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy
# Mon, 07 Mar 2022 21:03:33 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 07 Mar 2022 21:03:33 GMT
WORKDIR /home/groovy
# Wed, 09 Mar 2022 00:27:14 GMT
ENV GROOVY_VERSION=3.0.10
# Wed, 09 Mar 2022 00:30:11 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm -rf "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Wed, 09 Mar 2022 00:30:11 GMT
USER groovy
# Wed, 09 Mar 2022 00:30:13 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7418fdfb53d3b677d087a50df49ad12829a9eab2f0b2c8c19b162589387891`  
		Last Modified: Thu, 13 Jan 2022 17:22:44 GMT  
		Size: 430.3 KB (430278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae7b8c461b80a787226dfdd0673e9fe7036388862ea32248d15f6a14916f8be`  
		Last Modified: Mon, 07 Mar 2022 19:30:49 GMT  
		Size: 192.9 MB (192891714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f337ae9f87446e991566625212477c2cb66e4e5e3d653165ea9727e1c66bace`  
		Last Modified: Mon, 07 Mar 2022 19:30:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5023584b481b5f94712b4e29b886962753c43aed0d4a6b0a9a93c4fa192925`  
		Last Modified: Mon, 07 Mar 2022 21:06:30 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ad1c7da8ab70bd0d1cfe215ced5a3bbd918cf7925b58eedc9532fbd88ba986`  
		Last Modified: Wed, 09 Mar 2022 00:41:51 GMT  
		Size: 44.2 MB (44191529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc935545fa66b94589b207350546b7bd9ac5508a153fe1f60afa2a770fd7f5fc`  
		Last Modified: Wed, 09 Mar 2022 00:41:48 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
