## `groovy:jdk-alpine`

```console
$ docker pull groovy@sha256:286e2ad6eca7ceb04bff1a91461d7a15e49ff18aabb066b3b99e02f4596a1d3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:jdk-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:d1b4de79578b8304e6ff73c322b310fa69d78abc2609ad9678b3c3396d5fb7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (198005832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195a4cb70c39f0c47367547b3a7bf7a929458f0da821a66514a5789a9dfa7017`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb1617e759d446eb76924157e9d2a4abce94126e1aabca0005705104f883d0`  
		Last Modified: Tue, 14 Jan 2025 20:33:20 GMT  
		Size: 20.7 MB (20665909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d004dcd675c3245a83b07fc5bf7ef3c8e0d00fcbbb48fb5389af03d42fa51a56`  
		Last Modified: Wed, 08 Jan 2025 18:26:45 GMT  
		Size: 143.7 MB (143688926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee37ad4f4e20921436f927097031886033e13d06446534fa43e6052822ee74e`  
		Last Modified: Tue, 14 Jan 2025 20:33:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9eaba84656de704472f0a174bd1e39de0007ffd216ad4b5d9438717a5718152`  
		Last Modified: Tue, 14 Jan 2025 20:33:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decd9688ee8dd7b85dbc3f5029913bb8961b1025cb64febd940ee9836fd9d25a`  
		Last Modified: Wed, 08 Jan 2025 19:16:58 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfa0a9223c5cb090f53bcc54603fa11c0d4987ab67a669aed6beba31075d934`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 30.0 MB (30021113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86774b5452273e8df82522ae49b2341213c0ae0483ca5622208003e96e0a8995`  
		Last Modified: Wed, 08 Jan 2025 19:16:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:ea122eed5677c5881d555448a704b2cb9d02849beaeebdf63a7f3e31edde6506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27772c57dda55b63867b3bb6b7329ea1f1424de497ac5fc0984a7da0e621d277`

```dockerfile
```

-	Layers:
	-	`sha256:ccacc9869e37a828808a38417a0bc70d947b9179418d1c4904bd16146b366c92`  
		Last Modified: Wed, 08 Jan 2025 19:16:58 GMT  
		Size: 1.2 MB (1150310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015851bcf4bd8f463c83d7e7f8a1f2f6fa9e5ad6d14491df6fe8590d8c8317f4`  
		Last Modified: Wed, 08 Jan 2025 19:16:58 GMT  
		Size: 24.2 KB (24193 bytes)  
		MIME: application/vnd.in-toto+json
