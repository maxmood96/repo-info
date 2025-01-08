## `groovy:jdk17-alpine`

```console
$ docker pull groovy@sha256:e0bdffad260facedfb6260bfe9df6ea6f5bf8945bd52abd4aa8efbc2636fb0f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:jdk17-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:eed87fcb486765e7082ea05316f8e090b52fd64569cc874fffc3c39d1eaf3113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197974432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56452d260c5c5a423fbaac56f95da86545a3f818f772b1651b96f51e9688833`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='67632ee4563e9827b56f62ab6da95bce200d9e82092b211988c0d2113abc4071';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Sat, 09 Nov 2024 02:52:58 GMT
CMD ["groovysh"]
# Sat, 09 Nov 2024 02:52:58 GMT
ENV GROOVY_HOME=/opt/groovy
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sat, 09 Nov 2024 02:52:58 GMT
WORKDIR /home/groovy
# Sat, 09 Nov 2024 02:52:58 GMT
ENV GROOVY_VERSION=4.0.24
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
USER 1000:1000
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2596515a216afec869dba3c2bec5b62ba6c48118722dfbff7def49d152ea214d`  
		Last Modified: Tue, 07 Jan 2025 03:31:19 GMT  
		Size: 20.6 MB (20646952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b1aaac687d0c998775cd178cfcb63c4942a7cae3524abf72b2cb773ada6b6`  
		Last Modified: Tue, 07 Jan 2025 03:31:22 GMT  
		Size: 143.7 MB (143688951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c458e7badcfa1c296cf3de2ce32be91ebfc3e6c7af5bfcd4daf878398cdfa11`  
		Last Modified: Tue, 07 Jan 2025 03:31:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c5896dd8c5c1d3a7168bce341204f1cc3906f540b490bd5c36ca8902c86ba2`  
		Last Modified: Tue, 07 Jan 2025 03:31:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03fc9237d2b3d924bb846e723456af6a023d7d52f4fe3d5eedc039a87025d6e`  
		Last Modified: Tue, 07 Jan 2025 04:21:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150acf786b5570f0c1a66a8df0fdf83c56b5a59c7d28f35d84f8d91a8f23144d`  
		Last Modified: Tue, 07 Jan 2025 04:21:02 GMT  
		Size: 30.0 MB (30020903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a650fd14a889f3bc4266b85ac7b450fe183a887984b842e2af8b278105a6d504`  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:c05ea6845f5146e313ef95d576c694df0354727a33fa03d9bed0b04973965afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba8c979de356a33e4716f2aec67c311e5cb35540645c457011b7517fd48f653`

```dockerfile
```

-	Layers:
	-	`sha256:48cb6a515e18f2149141dc6ac332ca8e55fb8c6b36384344c24fa3d6385ff466`  
		Last Modified: Tue, 07 Jan 2025 04:21:02 GMT  
		Size: 1.1 MB (1144432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a05de5442f27885c4a8a358335d4aefc918a9a9a97d91a16b4f17af6164997`  
		Last Modified: Tue, 07 Jan 2025 04:21:01 GMT  
		Size: 24.2 KB (24192 bytes)  
		MIME: application/vnd.in-toto+json
