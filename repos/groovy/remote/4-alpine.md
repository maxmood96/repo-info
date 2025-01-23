## `groovy:4-alpine`

```console
$ docker pull groovy@sha256:83b50ec6562cc067a913efe22d59605706633f693607a79971ba92accef691ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:4-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:9a1ae205a1364f836642c1d6ca94a7b30c9b332cb70c6d0064f2e8b4f1e02d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198265629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626017c628d8c5a5f0081599d6e7928dfbe2f336e603075ab8e5edf55387e9d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sat, 09 Nov 2024 02:52:58 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
CMD ["/bin/sh"]
# Sat, 09 Nov 2024 02:52:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 Nov 2024 02:52:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Nov 2024 02:52:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='67632ee4563e9827b56f62ab6da95bce200d9e82092b211988c0d2113abc4071';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 09 Nov 2024 02:52:58 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8ac0524037a4eda23f7295f488c7798e164d787fdcd8357dcca0b4fc2137ee`  
		Last Modified: Wed, 22 Jan 2025 18:27:48 GMT  
		Size: 20.9 MB (20908664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa1b94f6a742fb709df97843970ae7c293892e396cbd5d0e74544dd5243e194`  
		Last Modified: Wed, 22 Jan 2025 18:27:50 GMT  
		Size: 143.7 MB (143688888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec922bc2dc31ed98aa0bf71cf9059f1f676b6d2e0af56ff5a0841825cdd8d3cf`  
		Last Modified: Wed, 22 Jan 2025 18:27:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9085af3d24e4ee3869258681600497e04f0d55f37be9c305dc9970cc976e5174`  
		Last Modified: Wed, 22 Jan 2025 18:27:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0efc7b2ee56b07de0d1cb21ab0bfbe76dd5f1200b2a491327f16e0f2ae768`  
		Last Modified: Wed, 22 Jan 2025 19:35:51 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a59d11992c76cc24a6b736012ac28e623cfb9833de828b3e4c46a129abf6b9`  
		Last Modified: Wed, 22 Jan 2025 19:35:52 GMT  
		Size: 30.0 MB (30022737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd480210da965cf2188b88ccdb9f7863961f22deed06caaee59d4afbbf74592`  
		Last Modified: Wed, 22 Jan 2025 19:35:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:8eb44472b77057d0ba76a35cef4facae2eca99b01a99a2c9300a881c547ece71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1205819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aed31c96285af8eb1dbdb4edd4ff7f34bd48376d11a1f126a9bbe2fd2779ce`

```dockerfile
```

-	Layers:
	-	`sha256:cbe8db3110d16e8256b4c9875e462f80a074cc34fe9ed116c51a75e33595cfbb`  
		Last Modified: Wed, 22 Jan 2025 19:35:51 GMT  
		Size: 1.2 MB (1181625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05ba8899ca13e5c5cafbd859088186ece95a5bf294ff6e385464e8e4e6db83f`  
		Last Modified: Wed, 22 Jan 2025 19:35:51 GMT  
		Size: 24.2 KB (24194 bytes)  
		MIME: application/vnd.in-toto+json
