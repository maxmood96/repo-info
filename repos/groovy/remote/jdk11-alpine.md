## `groovy:jdk11-alpine`

```console
$ docker pull groovy@sha256:7985c1a973d22ccf05c2ab3c0373cd9f5f654ea8d363ebf236e613f47126098d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:jdk11-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:c54b66a29736f93ea368a9242a1710822ef8283d732c1dbcd0f56aa9a3202627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183634211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac66dc67c45c889355890f93c2d48b0b843942addc0e0ec193e555cb6b61846`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ae988c72eeb2d78bb729a3387601ce0ea84305734ebdbe95d276f39952a8e019';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["jshell"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dff7dc6fc2858af0a16833a15a63741d58d895a9d1a9a2de411e9921a0de0dd`  
		Last Modified: Thu, 25 Jul 2024 17:25:18 GMT  
		Size: 9.4 MB (9394889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2a3080f55a0df9191af7a0a5db0289f1fb254d52b39af6fa1d3089b3292284`  
		Last Modified: Thu, 25 Jul 2024 17:28:06 GMT  
		Size: 140.7 MB (140723653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157f0a6d035e90e7a6e9bceb73fa7e2a378d545b4cc559693c03a0d4b3526f34`  
		Last Modified: Thu, 25 Jul 2024 17:27:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb69009c15daac0d6f12f9f460878fba3500b7afa91b063ba25de2db18180e9`  
		Last Modified: Thu, 25 Jul 2024 17:27:55 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed86db70e90ef273d9eb7513bb56268997174959de92261ebd08f4bb4d46d08a`  
		Last Modified: Thu, 25 Jul 2024 19:02:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac49dc31945190984dd6570f5e0ad4c83cb5d28fbbbf72d57e8af41ccd79fc8`  
		Last Modified: Thu, 25 Jul 2024 19:02:54 GMT  
		Size: 29.9 MB (29889536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fb847f7dfb566c52bcc41602ca3d05274f7889848e94a9f1bfab79fdb3fc3a`  
		Last Modified: Thu, 25 Jul 2024 19:02:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk11-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:7688de8417cfeb5a7d1510043be30ef0476656a5a4f6b4c75271225ac75f6d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **816.5 KB (816468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4f5403ce6abbe84056a285e0a7353728126f2788b39aca63700cbdfe8d51dc`

```dockerfile
```

-	Layers:
	-	`sha256:dc35d1e7e40b91434270fa91a9c95c602258e2f1fe9880f2cfc7f8c1ee8cde73`  
		Last Modified: Thu, 25 Jul 2024 19:02:53 GMT  
		Size: 794.5 KB (794493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df428bcb13c09f3109fac4803f5cb20ab07db7fd4294766a3ff94a35ce739348`  
		Last Modified: Thu, 25 Jul 2024 19:02:53 GMT  
		Size: 22.0 KB (21975 bytes)  
		MIME: application/vnd.in-toto+json
