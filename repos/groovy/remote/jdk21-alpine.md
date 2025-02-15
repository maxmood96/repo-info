## `groovy:jdk21-alpine`

```console
$ docker pull groovy@sha256:c55ccafa9f3aefa8bff3219f446cfc15fd7a727a98247bde42e1e53595cfd690
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:jdk21-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:4a14300b74609355daf99c3e39aefe1cd600c5a6df04660f1c9b008c8d754d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212460328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aad05fcbdc1e9815dd927679d8c07b1295bed65513b1d59d40890fa75c3668`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 28 Jan 2025 19:12:40 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 19:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 19:12:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='2798990401d9c47eaeddb7d5148f577770e4c1013b9223290a43765463204ae4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='6c66470a9143ad562570a34c1583d9fa50bf904f6f9ced642e9d800ce043a0f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["jshell"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["groovysh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 28 Jan 2025 19:12:40 GMT
WORKDIR /home/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_VERSION=4.0.25
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
USER 1000:1000
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2377dc8d3710b6bf7410a46adf016bdb060a8b4a7114189518f7f60fae85e3`  
		Last Modified: Fri, 14 Feb 2025 20:34:10 GMT  
		Size: 20.9 MB (20949767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79312d97e63a3dd5a83b89c90503f5d3c5c8ce261682999e1d12cf54506ac32`  
		Last Modified: Fri, 14 Feb 2025 20:34:22 GMT  
		Size: 157.8 MB (157796824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573882c363c812b21ff606ea7d12eff8720580a29a875238f127d7f80b9f0da1`  
		Last Modified: Fri, 14 Feb 2025 20:34:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1f65d07a350139d7390033a591e07d865c082f4b458bb56ff38bc143349c8`  
		Last Modified: Fri, 14 Feb 2025 20:34:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb3cf61c11f03a8ea3c2a13ccf69cc8622cb27c31bc121eca7dcd7f0e38d2a5`  
		Last Modified: Sat, 15 Feb 2025 00:21:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbe9127087e61ceb6bab31725be068c99319362cf27aa893718be47a871cb91`  
		Last Modified: Sat, 15 Feb 2025 03:07:00 GMT  
		Size: 30.1 MB (30067877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd65408fb4d644a098991ea901160a9428feaa032fcba55b08b359cc2e0577d`  
		Last Modified: Sat, 15 Feb 2025 03:07:00 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:9050c32b98f861a417f3bcf5b805a0fb949b6488a18cc533a69034d0ef43bcde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1204603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28de6710e36fce8d0580ee794b45c877dc4697991b7572249d8bb5734b9788f6`

```dockerfile
```

-	Layers:
	-	`sha256:9a90958b7652449313f771c7ba1881390619774731a9ba9a4e56d049849f6fd9`  
		Last Modified: Sat, 15 Feb 2025 00:20:41 GMT  
		Size: 1.2 MB (1182573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845d73ab5031132aedcd52f9b4138e1ea29f0f340c297bbc9079a28ff43c8cc6`  
		Last Modified: Sat, 15 Feb 2025 00:20:41 GMT  
		Size: 22.0 KB (22030 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:57c80a7faf58eb0cfd266754b01864aba2238ab48a0880c800b3156b08ddc07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210866477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99085a3228a7ef4d123f3c45bfea0ddcb9eb235a4e9a2cff6bc91f540bd04663`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 28 Jan 2025 19:12:40 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 19:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 19:12:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='2798990401d9c47eaeddb7d5148f577770e4c1013b9223290a43765463204ae4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='6c66470a9143ad562570a34c1583d9fa50bf904f6f9ced642e9d800ce043a0f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["jshell"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["groovysh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 28 Jan 2025 19:12:40 GMT
WORKDIR /home/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_VERSION=4.0.25
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
USER 1000:1000
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22460361c4e9e1ac6bf5bc45209d88abdf89352662d6ea415fdaae2281c39acd`  
		Last Modified: Sat, 15 Feb 2025 01:18:42 GMT  
		Size: 21.0 MB (21005533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d006405dd14f86430a341fc9e96608553ddc4de8ca7c21843b389282b46a2`  
		Last Modified: Sat, 15 Feb 2025 01:18:56 GMT  
		Size: 155.8 MB (155787997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3703c2f380b3b4e3eeae969e60074a2cce6d72889dc412466f29ef5ebfc440f7`  
		Last Modified: Sat, 15 Feb 2025 01:18:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060a7bd90d15285d6041f307b0a65f5415677f1d9d59e445a6c3b5b27f5f9cc0`  
		Last Modified: Sat, 15 Feb 2025 01:18:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed82e886a9b70566e8a04c10051280bb71a7557be8dfcab868428d031add6e1`  
		Last Modified: Sat, 15 Feb 2025 07:23:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03d3138d441cc72e59652f8ea2b81031e5cf36711ab80efb8556f155ed487cc`  
		Last Modified: Sat, 15 Feb 2025 07:23:13 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0149f6b79995c29a4c05909b8e13e760b092111744626faab1fd0839ad7e9fec`  
		Last Modified: Sat, 15 Feb 2025 07:23:12 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:20b31451d4ea523b556bbbb97510b41dc32f6c60171e8252dbbcbbe2a64b853b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1354726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b20b1e956362be39a9963e56f6879c01947277f4927758b697131c98cd88f9`

```dockerfile
```

-	Layers:
	-	`sha256:d3231fcf4db6ef083a02634b563721e3ec79635b2b5c6b575db8283f589c5740`  
		Last Modified: Sat, 15 Feb 2025 09:20:30 GMT  
		Size: 1.3 MB (1332575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f086dfa3966a80e421d704eca707c0debfffb14f1769cf27552ad1e2520ee49e`  
		Last Modified: Sat, 15 Feb 2025 09:20:30 GMT  
		Size: 22.2 KB (22151 bytes)  
		MIME: application/vnd.in-toto+json
