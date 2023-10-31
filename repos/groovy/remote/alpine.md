## `groovy:alpine`

```console
$ docker pull groovy@sha256:dfb7726bb3d67e3d0c3c35561e7b5de9ca230523217a0285074568e46629be98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `groovy:alpine` - linux; amd64

```console
$ docker pull groovy@sha256:eeac98c138b0ac95ca120bb41e0c9cf44f15f85748d9e01a7a9a5c2f5898a57f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190395507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6c65cf77a06369ce72b880ec1046abcb63e82273f00c78c15e43c59fd0c1fb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

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
# Mon, 30 Oct 2023 23:26:31 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:26:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c2a571a56e5bd3f30956b17b048880078c7801ed9e8754af6d1e38b9176059a9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 30 Oct 2023 23:26:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:26:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:26:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:26:42 GMT
CMD ["jshell"]
# Tue, 31 Oct 2023 01:33:00 GMT
CMD ["groovysh"]
# Tue, 31 Oct 2023 01:33:00 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 31 Oct 2023 01:33:00 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy
# Tue, 31 Oct 2023 01:33:00 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 31 Oct 2023 01:33:00 GMT
WORKDIR /home/groovy
# Tue, 31 Oct 2023 01:33:01 GMT
ENV GROOVY_VERSION=4.0.15
# Tue, 31 Oct 2023 01:33:11 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm -rf "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Tue, 31 Oct 2023 01:33:11 GMT
USER 1000:1000
# Tue, 31 Oct 2023 01:33:12 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
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
	-	`sha256:d7937dfaa0fb6ed551351b36347ca4eb7da6b03baa8d9d2991f0bd28df58b863`  
		Last Modified: Mon, 30 Oct 2023 23:35:28 GMT  
		Size: 144.1 MB (144111175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec44800a653716150002cf7731ab02425d333379727abe1a4bdfd0ebf6d66c8`  
		Last Modified: Mon, 30 Oct 2023 23:35:17 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5fcbc2e814b463720991d75d84f18f6d5b50993c1e8bff08d97c4d59be6f14`  
		Last Modified: Mon, 30 Oct 2023 23:35:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69855e614679f155e252952849eba89df53cd741d952185dcc596abe504c1512`  
		Last Modified: Tue, 31 Oct 2023 01:35:46 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef539a1014d0e1cbf238bdd9edd85eb29018e3f838f0e1631de581e353eb175`  
		Last Modified: Tue, 31 Oct 2023 01:35:48 GMT  
		Size: 29.7 MB (29738900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7e897dd592088607f87b001c002b2ce6feb44a87b1e7766e44b239feb46667`  
		Last Modified: Tue, 31 Oct 2023 01:35:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
