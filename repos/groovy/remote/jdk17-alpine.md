## `groovy:jdk17-alpine`

```console
$ docker pull groovy@sha256:3ee4eedae740ea35614e62ccaca949c723ff3a3a84c30bcdb5d990b825463f97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:jdk17-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:bedc354e9f19a64214165941c3634e5a9e9ac54a6c980a0f2177b6c5cc9c7eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191952523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4154b5c0a557fbf6d1103a2c490e32e546a31a6ab54eb7c77fa3422cef1c91c6`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:479e64820c602a6421582ff22341d66b5c6938bee2115d203f3d03147a89505e`  
		Last Modified: Thu, 25 Jul 2024 17:29:26 GMT  
		Size: 14.0 MB (14039136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e384a19a9b0cde9f53fc5c79a581f80b1606cb9b0c477b8019b1716ffe026fe`  
		Last Modified: Thu, 25 Jul 2024 17:29:36 GMT  
		Size: 144.4 MB (144394552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed71e81fa34c6c2e7902182aaf9da971d499b0e58d2dfcc2c789535bc6768e0`  
		Last Modified: Thu, 25 Jul 2024 17:29:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9ed14297063e3f9d673e7701f762b7d77112fe3f472e8b50399411d45457a`  
		Last Modified: Thu, 25 Jul 2024 17:29:24 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2531d60ac51ac072c5c9ff87f932c6d464aa6eb204f15ae9e16beda2386a4f1`  
		Last Modified: Thu, 25 Jul 2024 19:02:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd47670b56a95b636f37b9d6f819a2432c331a081eb5c0d01a5256f8e56b604`  
		Last Modified: Thu, 25 Jul 2024 19:02:50 GMT  
		Size: 29.9 MB (29892702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b6625f501a3eceb0134fc7ab9f773d1efbfe900c686147652c07a9f2ff493`  
		Last Modified: Thu, 25 Jul 2024 19:02:50 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:bfcb4f5f60b987ebf580f5072d3811a05f68a96badf07a9bbb8354e2131ab6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.2 KB (917230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333ac47c442717d17ba90229d17aa0ba2cb55b578511eb07cda3ad16269247e0`

```dockerfile
```

-	Layers:
	-	`sha256:1e6b9d3d0e5918a0c80074205126b279e3e262e08590ad640fd823ea44ea35a5`  
		Last Modified: Thu, 25 Jul 2024 19:02:49 GMT  
		Size: 893.1 KB (893092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22852e6b4ca5c44c015014bfc5c3ead71ec25945743cc936a81831dac38aca68`  
		Last Modified: Thu, 25 Jul 2024 19:02:49 GMT  
		Size: 24.1 KB (24138 bytes)  
		MIME: application/vnd.in-toto+json
