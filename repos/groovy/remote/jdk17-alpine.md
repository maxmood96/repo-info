## `groovy:jdk17-alpine`

```console
$ docker pull groovy@sha256:b999bf9565510535bb4af1df517ffad0bbdc4de7a53da5768bf7b8e89181098f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:jdk17-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:9616d7abda06e9d9271a8fdd9e779b4d27fd05cf6227b4c3b3083c2b0827864c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204838444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50adab838f5f16baca830576dcaaf29c6628fb598f3cd8d3e5b2bcab5842cab0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:58:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='960b4090b75a887bb21a915a294bee3a97cd11876967c95e5bd29d9ec4812e17';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:58:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:58:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:58:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:58:43 GMT
CMD ["jshell"]
# Wed, 13 May 2026 17:55:23 GMT
CMD ["groovysh"]
# Wed, 13 May 2026 17:55:23 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 13 May 2026 17:55:23 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 13 May 2026 17:55:23 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 13 May 2026 17:55:23 GMT
WORKDIR /home/groovy
# Wed, 13 May 2026 17:55:23 GMT
ENV GROOVY_VERSION=5.0.6
# Wed, 13 May 2026 18:00:28 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 13 May 2026 18:00:28 GMT
USER 1000:1000
# Wed, 13 May 2026 18:00:29 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b50ae58d435408a9b026fe52e1670bc1fa8333eabfe9bf8732808b503921e21`  
		Last Modified: Thu, 07 May 2026 23:58:58 GMT  
		Size: 21.3 MB (21336223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0d10cee20aac36e35f4a5f8b5277bf42d4cb4c8d9a9d4fcdccdc80bc721a6`  
		Last Modified: Thu, 07 May 2026 23:59:01 GMT  
		Size: 145.1 MB (145051725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e55ba8d37d6d0466dfc5f33fb9646c28947c3dc8386294a7f1f12a35edc2c`  
		Last Modified: Thu, 07 May 2026 23:58:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665e255b26ac403ea595f439a3807b4421a1347f75ad3570ce930c2ea8a8a4a6`  
		Last Modified: Thu, 07 May 2026 23:58:57 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74a4831f6f18a72a3a930f71a6734b35d32ffda9c0bce2ed6824ca1e465ac79`  
		Last Modified: Wed, 13 May 2026 18:00:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b43eaee50a8a21fe5d680d66d64874f5f9dd2bd1c6cc5da6694280c00fd31e`  
		Last Modified: Wed, 13 May 2026 18:00:40 GMT  
		Size: 34.6 MB (34582693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b3113dbf94230195ac4d4aca817b4a55d5ed5f0d3a2676627c52c8dbe2e61c`  
		Last Modified: Wed, 13 May 2026 18:00:39 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:8cb9796248a32f19aa86d139ca4abe275d2cec4057066f6780af9ed31230f0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1228379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5e7049c90fdf1595e09f3b96cc24d399ac8a9764374fd7046e9fb446c377ad`

```dockerfile
```

-	Layers:
	-	`sha256:f808e67de7804d6e3dfb6dfa2af9d1f41bacd40ebebe820665fbca37af1501e0`  
		Last Modified: Wed, 13 May 2026 18:00:39 GMT  
		Size: 1.2 MB (1206049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b5dd0ee55521bd0ea3218b59fd0d7ec90b4579c5242498da17134f2b30bcb74`  
		Last Modified: Wed, 13 May 2026 18:00:39 GMT  
		Size: 22.3 KB (22330 bytes)  
		MIME: application/vnd.in-toto+json
