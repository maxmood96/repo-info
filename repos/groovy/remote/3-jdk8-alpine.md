## `groovy:3-jdk8-alpine`

```console
$ docker pull groovy@sha256:e3320b4958523f224a45443dd76258b28e3906474fa14fb20b4408209e03bd80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:3-jdk8-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:44e93a7b6914febfe1cfc6083920d6187c47529f658e23b680d7827b400087dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149654496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32de5bbd4e7312ef339ba45cf0e7351b07091bd8583215a89e924da22af629ee`
-	Default Command: `["groovysh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:42 GMT
ARG version=8.492.09.2
# Mon, 22 Jun 2026 19:53:42 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:53:42 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:53:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:53:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 22 Jun 2026 20:20:39 GMT
CMD ["groovysh"]
# Mon, 22 Jun 2026 20:20:39 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 22 Jun 2026 20:20:39 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 22 Jun 2026 20:20:39 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 22 Jun 2026 20:20:39 GMT
WORKDIR /home/groovy
# Mon, 22 Jun 2026 20:20:39 GMT
ENV GROOVY_VERSION=3.0.25
# Mon, 22 Jun 2026 20:25:31 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Mon, 22 Jun 2026 20:25:31 GMT
USER 1000:1000
# Mon, 22 Jun 2026 20:25:31 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f3c4d4c9c4dedbfb87c6fd93779b4557362fa6c8ecb6c2c79586261408603e`  
		Last Modified: Mon, 22 Jun 2026 19:53:56 GMT  
		Size: 100.8 MB (100751407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a8b5d8472c96083b871d4c3045633e71ca91d76bd9e5114bfb3cf2167baf6b`  
		Last Modified: Mon, 22 Jun 2026 20:25:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a586e7d1d91f1e8509363f62e02ed887c3a0263575eb7e5eca9c9e6ee726a8`  
		Last Modified: Mon, 22 Jun 2026 20:25:41 GMT  
		Size: 45.1 MB (45057469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a8ed6a24848f4355d4becd5bbff4dd291cff20fba45fd3611c99fd69cf62e2`  
		Last Modified: Mon, 22 Jun 2026 20:25:39 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:3-jdk8-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:e8149c14bc395598fb0c9ce30044c083598f4eae757ed1132b8964ea687dcd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 KB (392125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415681926675168d116398641ba0b9b4fb4829f78b235e1e053b636f01aa6616`

```dockerfile
```

-	Layers:
	-	`sha256:378c17df1a3524d3a3177090547c4802c1af5c9fecf7ab6aebbb265364982758`  
		Last Modified: Mon, 22 Jun 2026 20:25:39 GMT  
		Size: 373.1 KB (373091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4407eb4c4f1d07a2476590f6baeb5efc9619ee31a284f00041df5e5d4357a83`  
		Last Modified: Mon, 22 Jun 2026 20:25:39 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:3-jdk8-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:80b4bbaef1214e7d17fb846600887fb449f6abbd883b96a316efe9c179b17d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149785309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d45720a7313f115828ae931def959a4cd8e44f7067db51b2d57d839547fb415`
-	Default Command: `["groovysh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:11 GMT
ARG version=8.492.09.2
# Mon, 22 Jun 2026 19:55:11 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:55:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 22 Jun 2026 20:56:06 GMT
CMD ["groovysh"]
# Mon, 22 Jun 2026 20:56:06 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 22 Jun 2026 20:56:06 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 22 Jun 2026 20:56:06 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 22 Jun 2026 20:56:06 GMT
WORKDIR /home/groovy
# Mon, 22 Jun 2026 20:56:06 GMT
ENV GROOVY_VERSION=3.0.25
# Mon, 22 Jun 2026 20:56:44 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Mon, 22 Jun 2026 20:56:44 GMT
USER 1000:1000
# Mon, 22 Jun 2026 20:56:45 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acebb8a27a8a24e1782e5c771db390498b6dbf05653299f2dc32dce10ec19d9`  
		Last Modified: Mon, 22 Jun 2026 19:55:26 GMT  
		Size: 100.5 MB (100544823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd38c2e4a49092e3af80476ebe0a19c10db1dfbb0317f197258b5a9f948f5f1`  
		Last Modified: Mon, 22 Jun 2026 20:56:31 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb8ce499f6144ca615d1ec9c0b99f170e8fcdca6eea22e1309ff30de4a38202`  
		Last Modified: Mon, 22 Jun 2026 20:56:56 GMT  
		Size: 45.1 MB (45057426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f532d2952dfd3f051971a1208285a88f7affcdf9e57275e39facfc1ed9d2b3`  
		Last Modified: Mon, 22 Jun 2026 20:56:54 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:3-jdk8-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:088eeb5abf55c6bec07593c7756ec2e224cdd5ea0d96549c45ab1763e1fd1f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 KB (391716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6289f704e2f64555ee5f5e8fb3002ab1455f5d24d389f95fb37df16b7fce91`

```dockerfile
```

-	Layers:
	-	`sha256:ff4a89e480707d1c652051c309a02d5a64ac49615afa6eb01a150f3af878663e`  
		Last Modified: Mon, 22 Jun 2026 20:56:54 GMT  
		Size: 372.6 KB (372561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca6fb6441c60d6d3547f1fcacab0bbd441d0a69261d8a249ca32623cd80dc45`  
		Last Modified: Mon, 22 Jun 2026 20:56:54 GMT  
		Size: 19.2 KB (19155 bytes)  
		MIME: application/vnd.in-toto+json
