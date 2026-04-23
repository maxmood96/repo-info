## `groovy:jdk8-alpine`

```console
$ docker pull groovy@sha256:c3e3f0c59a5d02b5f3e672701db03bc17cc0ef779bd224959907a7ae58f38432
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:jdk8-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:60ac3b4a06e7afaa70cb78f0559f45514f49c0ec3fb1f65aaddb1462b38c56c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134996595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f086272d468239e8917463f74c12ce512a64c523471cec0b91f76bb9beb9bc6`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:09 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:09 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:12:46 GMT
CMD ["groovysh"]
# Wed, 22 Apr 2026 22:12:46 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 22 Apr 2026 22:12:46 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 22 Apr 2026 22:12:46 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 22 Apr 2026 22:12:46 GMT
WORKDIR /home/groovy
# Wed, 22 Apr 2026 22:12:46 GMT
ENV GROOVY_VERSION=4.0.30
# Wed, 22 Apr 2026 22:12:56 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 22 Apr 2026 22:12:56 GMT
USER 1000:1000
# Wed, 22 Apr 2026 22:12:56 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228516198dcf71bb7973cf0e588a55b084e664ca989f408ecf3dd4a0ff9f028d`  
		Last Modified: Wed, 22 Apr 2026 21:33:25 GMT  
		Size: 100.8 MB (100787224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf4f9ac929ef092304035eceb830267a57393859cd733292df5db86f1b766aa`  
		Last Modified: Wed, 22 Apr 2026 22:13:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b1ab1142edc9eb41088d014f88fbcc7aa74daf3607818fc9d3a76c81605543`  
		Last Modified: Wed, 22 Apr 2026 22:13:05 GMT  
		Size: 30.3 MB (30343982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fee57213ac596db63101f5383fd5020bef8d79982a0fb7ebfd78c9edf8fdd87`  
		Last Modified: Wed, 22 Apr 2026 22:13:04 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:04f22f548a7ed054a40d81436b71045d914fb418ea6c793b778af519913bc040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25f85aaa60929951b820356b5b43fdc4e5865c5b9bbb9535123ad0187b3da7f`

```dockerfile
```

-	Layers:
	-	`sha256:05d244b3c731945b9c9ceeb2d2455a594f1f75184fba18c191aaf42c413045e9`  
		Last Modified: Wed, 22 Apr 2026 22:13:04 GMT  
		Size: 331.3 KB (331322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f3b8631fac64ef722b844fb6271a552acc8811ce1416d87345b1eb02bc50fa`  
		Last Modified: Wed, 22 Apr 2026 22:13:04 GMT  
		Size: 19.3 KB (19342 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:0e263f065af3a0c6476eca9f0843a2a29d53ded27ecfd882a85c919ac34cb2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135116584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe6ba71677dbd0c9f66f3bed26c6faaedbe7e489e8eaeadd20db2f9bc3397c9`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:16 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:16 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:16 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:12:35 GMT
CMD ["groovysh"]
# Wed, 22 Apr 2026 22:12:35 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 22 Apr 2026 22:12:35 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 22 Apr 2026 22:12:35 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 22 Apr 2026 22:12:35 GMT
WORKDIR /home/groovy
# Wed, 22 Apr 2026 22:12:35 GMT
ENV GROOVY_VERSION=4.0.30
# Wed, 22 Apr 2026 22:12:51 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 22 Apr 2026 22:12:51 GMT
USER 1000:1000
# Wed, 22 Apr 2026 22:12:51 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcce3fd15c9d9eafd7fb5c5782c31fca73f6c459593a4bcb43e6b505a41d156d`  
		Last Modified: Wed, 22 Apr 2026 21:33:31 GMT  
		Size: 100.6 MB (100571524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a004d38d69f75ef3eaa020e4ac8e9759e35b78a0c375b555eac3bdbf6dd99e`  
		Last Modified: Wed, 22 Apr 2026 22:12:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fe2f8ea83e6bc0d6c12fc5aef15bf233d2e17f1266daa12bd6eec18b1c4bc1`  
		Last Modified: Wed, 22 Apr 2026 22:13:00 GMT  
		Size: 30.3 MB (30343990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121914e41ca4e6adec29c513d5ea29a97589b1305777567db1a6d241750323cc`  
		Last Modified: Wed, 22 Apr 2026 22:12:59 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:184fae731b647fb95c36fb14f1d83e858fba96473941c6125d9cfa430092e62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 KB (350278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d91165f5fd791ab7152991f1c2391435d0df34a188a5ef95b1cb79407eaa94`

```dockerfile
```

-	Layers:
	-	`sha256:202df669a4eec68b682ef04092f57b63305d4f51f3ea86457a0ab52ecdd44e10`  
		Last Modified: Wed, 22 Apr 2026 22:12:59 GMT  
		Size: 330.8 KB (330804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0d6e2aaae4889739c8b790872f4ba9940a49641aecc7fbf4a7284798a48904`  
		Last Modified: Wed, 22 Apr 2026 22:12:59 GMT  
		Size: 19.5 KB (19474 bytes)  
		MIME: application/vnd.in-toto+json
