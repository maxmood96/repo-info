## `groovy:jdk-alpine`

```console
$ docker pull groovy@sha256:dca06b8be4e8a71e9b0a0bff32e2c4613f5a9c2dfba4aea3da51747f374655f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:jdk-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:4354223f5d4383943e670a8e623022fd2b90262f55564117586f8806182b1b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217580457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6288a4113ebc94ea73753c42d410f57b9a82d28ae5756feb425c3f61f2baf15d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:09 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:16 GMT
CMD ["jshell"]
# Thu, 22 Jan 2026 18:38:41 GMT
CMD ["groovysh"]
# Thu, 22 Jan 2026 18:38:41 GMT
ENV GROOVY_HOME=/opt/groovy
# Thu, 22 Jan 2026 18:38:41 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Thu, 22 Jan 2026 18:38:41 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Thu, 22 Jan 2026 18:38:41 GMT
WORKDIR /home/groovy
# Thu, 22 Jan 2026 18:38:41 GMT
ENV GROOVY_VERSION=5.0.4
# Thu, 22 Jan 2026 18:39:26 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Thu, 22 Jan 2026 18:39:26 GMT
USER 1000:1000
# Thu, 22 Jan 2026 18:39:27 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c946e03558d5b63598812078583a7cacf7c19412e2c71732c6c7e972a09e0`  
		Last Modified: Sat, 08 Nov 2025 17:59:31 GMT  
		Size: 21.1 MB (21112184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34da1dc78644035d0dc76bd344bb33911551088d2c35e5eae20ee0883291ece`  
		Last Modified: Sat, 08 Nov 2025 17:59:34 GMT  
		Size: 158.1 MB (158102933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a3991c44d0e9016c97a7a16b122fc35778b7bf3abb694a7acabc5f8e6551c8`  
		Last Modified: Sat, 08 Nov 2025 17:59:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cb030eff3c05fd59aaea4464781aa26b800aef5bdbe8b20be44289a6d4fde7`  
		Last Modified: Sat, 08 Nov 2025 17:59:30 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad76ad449352f8af1b965966924aeff86cf7800c5ae1603530fd96108f9645af`  
		Last Modified: Thu, 22 Jan 2026 18:39:37 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ff858a50b42f57969afaf57529f2d30d1300780520dbf16188c2179b870b0e`  
		Last Modified: Thu, 22 Jan 2026 18:39:38 GMT  
		Size: 34.6 MB (34559276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2175ca2a8f734b97a9c2495dd1ac90587e3a7bc71c06e675f5782782ae485a6d`  
		Last Modified: Thu, 22 Jan 2026 18:39:37 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:1d723166feaacfe4e0071979b0af14d7df2080b157bf295b650dc0053fcea8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1233882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03eea59cbfbd9a0ce46a8c114a0528df9bc5652ac5c65818ed8e1209abb67a7`

```dockerfile
```

-	Layers:
	-	`sha256:0b493effd3f89da3966282d3f27792d51b7741beb1900d8a79267bc3a58d061f`  
		Last Modified: Thu, 22 Jan 2026 18:39:37 GMT  
		Size: 1.2 MB (1209123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541dd93b8e3a2cc9a3cc4a24c6309f75813c84d428f9dc825f4c8b64de9936f1`  
		Last Modified: Thu, 22 Jan 2026 18:39:37 GMT  
		Size: 24.8 KB (24759 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:9aea2a8e5ebd3c5c9a84049a87c454329a94fc91976de4b42ae0f0d3a02bc402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215976882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910eb0abfe1266f4ef2bcf80a9cddc66009280e21a2166d7c68b7ea765bb065`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:56:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:56:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:56:37 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:56:37 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 02:56:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:47 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 04:35:01 GMT
CMD ["groovysh"]
# Wed, 28 Jan 2026 04:35:01 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 28 Jan 2026 04:35:01 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 28 Jan 2026 04:35:01 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 28 Jan 2026 04:35:01 GMT
WORKDIR /home/groovy
# Wed, 28 Jan 2026 04:35:01 GMT
ENV GROOVY_VERSION=5.0.4
# Wed, 28 Jan 2026 04:35:09 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 28 Jan 2026 04:35:09 GMT
USER 1000:1000
# Wed, 28 Jan 2026 04:35:10 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237401997b4e6d77e1a6cbf3006b196170369b2872d0a2fba9f845ce7cfeeb5`  
		Last Modified: Wed, 28 Jan 2026 02:57:03 GMT  
		Size: 21.2 MB (21166024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf8a9ded26681fc49549c27c20edd4b88472a3ca476e9a7c4ebf9d58174315`  
		Last Modified: Wed, 28 Jan 2026 02:57:06 GMT  
		Size: 156.1 MB (156097479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9c000864d8ab5dc2884668139fc08c3b2e6cc3aaa69eacd03144943b90354f`  
		Last Modified: Wed, 28 Jan 2026 02:57:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e39acec808282ee08cd7b6292bf85d7b6775f69ca5e3bb0eb617e09e97bb94d`  
		Last Modified: Wed, 28 Jan 2026 02:57:02 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5e6e555113955a019531f32bba01df17e0160b53f34411d0c58f084afffcbf`  
		Last Modified: Wed, 28 Jan 2026 04:35:19 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7b191d4978fc1c3106539599db18884d7bd0c859926d3a2406d7bc2f271884`  
		Last Modified: Wed, 28 Jan 2026 04:35:20 GMT  
		Size: 34.6 MB (34570247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931f74f5b7466686e473d831087f610a869317f3b9b22f012a1420d1fcae2c0b`  
		Last Modified: Wed, 28 Jan 2026 04:35:18 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:573f44b42b6286b2c5ea71cc9a2655392f5cb46b7699411496b7b2d330a2dd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1384223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6038e714acf6e08ca68b0abee640bb1adb1b1765e3c5485fd2a9a94b38c2c7f`

```dockerfile
```

-	Layers:
	-	`sha256:3c3a055147502d21bc8a0d1b33bdb99c685ea97d0fe1c54619593cb5be523041`  
		Last Modified: Wed, 28 Jan 2026 04:35:18 GMT  
		Size: 1.4 MB (1359233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cd9432d5b9a2c79ff5fe657ea3c46184778901f28ecad8d6374a72b3cc250a5`  
		Last Modified: Wed, 28 Jan 2026 04:35:18 GMT  
		Size: 25.0 KB (24990 bytes)  
		MIME: application/vnd.in-toto+json
