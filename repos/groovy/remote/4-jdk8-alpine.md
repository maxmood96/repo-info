## `groovy:4-jdk8-alpine`

```console
$ docker pull groovy@sha256:60e93135f87b195f8ad6f77795bc99c301464e67750f9ac6bfa4eeddc2d5998d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:4-jdk8-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:9faa6b132d9b21ea1457c605f06ba6ffb574e07157b2ee1200c56bb1d6919f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134962326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa7fd428a7109c73aba6361292d2a9d37f20319d993b397522989a525474ff`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:58:42 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:58:42 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:58:42 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:58:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:58:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 13 May 2026 17:59:34 GMT
CMD ["groovysh"]
# Wed, 13 May 2026 17:59:34 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 13 May 2026 17:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 13 May 2026 17:59:34 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 13 May 2026 17:59:34 GMT
WORKDIR /home/groovy
# Wed, 13 May 2026 17:59:34 GMT
ENV GROOVY_VERSION=4.0.32
# Wed, 13 May 2026 18:04:14 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 13 May 2026 18:04:14 GMT
USER 1000:1000
# Wed, 13 May 2026 18:04:15 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78799819c2ab46aaeea7584a6e63546f8614eabfc576be9cb56de175814cb8`  
		Last Modified: Fri, 08 May 2026 22:58:56 GMT  
		Size: 100.8 MB (100751417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b694a541a543a84f6a34152aab3bfd0c17c8be904338bd804538d8f2c7903ad9`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02d8897e924a3010e94731a35dc916bfd93d589b56bd2742cd2e38703e2677c`  
		Last Modified: Wed, 13 May 2026 18:04:24 GMT  
		Size: 30.3 MB (30345516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed79ce824679203b30945228dc721aadaf9182f9f4d0b8e25a55fc17ee834ba1`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk8-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:f2eec2fbcd08bdb62aabb24855b1d7181f952ebbfb0e000b8346b4e8f81e063a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c1652f95714954d324a2f277555eaa9377a4f19893166223f2f17bef8967a`

```dockerfile
```

-	Layers:
	-	`sha256:a2903328109543fc132baa1d3f3c54f5a6a70039d70149319b9b30cb71e0b1f6`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 331.3 KB (331322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f75f96430e63b579d5d22f7c3993ab09883afa6b6717b8c9b9cb32589aa57f10`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 19.3 KB (19342 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk8-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:90e94b28195679733efc5eab32cecb8dd1dc5a56dd210d53f6a4ae7f044da5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135091270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f22b3a6d3c1f3408b43b6b82b1945fbdd20ceac2161b551fb97469e504d91f3`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:37 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:37 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:37 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:48:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 13 May 2026 17:56:37 GMT
CMD ["groovysh"]
# Wed, 13 May 2026 17:56:37 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 13 May 2026 17:56:37 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 13 May 2026 17:56:37 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 13 May 2026 17:56:37 GMT
WORKDIR /home/groovy
# Wed, 13 May 2026 17:56:37 GMT
ENV GROOVY_VERSION=4.0.32
# Wed, 13 May 2026 18:02:19 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 13 May 2026 18:02:19 GMT
USER 1000:1000
# Wed, 13 May 2026 18:02:19 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2b2750547d1382e8902a58f482ede14d5484098b6dbba6954feb54a9e3dbe3`  
		Last Modified: Fri, 08 May 2026 22:48:51 GMT  
		Size: 100.5 MB (100544688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88841aa232df80356ac77250f644a8c2bc1373d5cf4ff4ea2e611c05ab88679`  
		Last Modified: Wed, 13 May 2026 18:02:27 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccf69196a31b7a5582d66f004cf0d26fdbf6176efc31dbfd979d944b8af5546`  
		Last Modified: Wed, 13 May 2026 18:02:29 GMT  
		Size: 30.3 MB (30345509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd646298f625757ff0978e8ab9968a2138febb2e423705e11e375891b3d3129`  
		Last Modified: Wed, 13 May 2026 18:02:27 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk8-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:7554fbf844469ca0e42f51200cdac5f9706ee0240bc04db94a9983d6df044370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 KB (350279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8741e660b3589b0acdfaf632c5a76ecdde374dbc3fe6dde16d8037b7a3370376`

```dockerfile
```

-	Layers:
	-	`sha256:4271c8d13754455a05f5aaf250fe959b7ccfd176185eb0661104ff7d0a97af38`  
		Last Modified: Wed, 13 May 2026 18:02:27 GMT  
		Size: 330.8 KB (330804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117762c6c55d7f065a1b7582a1337afeb6b675ac01e8e8835d00414afec6ef96`  
		Last Modified: Wed, 13 May 2026 18:02:28 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json
