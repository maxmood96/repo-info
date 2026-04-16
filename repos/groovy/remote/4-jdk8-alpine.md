## `groovy:4-jdk8-alpine`

```console
$ docker pull groovy@sha256:36f8ef8127d77e262a517ad4d5047294500e0628a796ce47b805d76dfb81250a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:4-jdk8-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:783fda82f632c5d9b02e2d59b7e4a0cc4585dc043631cc1c9546550a71028dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134986278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b808e35452a4f461546bae92a0a704824293e2321adf054d4bb23aa5763b5b29`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:14 GMT
ARG version=8.482.08.1
# Wed, 15 Apr 2026 20:24:14 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:14 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:24:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:33:19 GMT
CMD ["groovysh"]
# Wed, 15 Apr 2026 21:33:19 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 15 Apr 2026 21:33:19 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 15 Apr 2026 21:33:19 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 15 Apr 2026 21:33:19 GMT
WORKDIR /home/groovy
# Wed, 15 Apr 2026 21:33:19 GMT
ENV GROOVY_VERSION=4.0.30
# Wed, 15 Apr 2026 21:33:27 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 15 Apr 2026 21:33:27 GMT
USER 1000:1000
# Wed, 15 Apr 2026 21:33:28 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88d1dcb40680cc470fb6c04d2b258ef4349b55286064027930674dd42c7a614`  
		Last Modified: Wed, 15 Apr 2026 20:24:28 GMT  
		Size: 100.8 MB (100776894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b500446983728aee77f05f14e4cb2d98deddac5fabbef2845b2653dee0c2823a`  
		Last Modified: Wed, 15 Apr 2026 21:33:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1d2397500df5b985c99821d4253bc3cedcdf75fece3f1ee38d3fcc00a73570`  
		Last Modified: Wed, 15 Apr 2026 21:33:37 GMT  
		Size: 30.3 MB (30343993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381edf39f6047ee34399d46f9a72665d43a1a5204042b6a73d7e81affa4b37a8`  
		Last Modified: Wed, 15 Apr 2026 21:33:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk8-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:e7b1d9c7754466f670c67c34ecfdd4782434b20bbce83d87146fc4e593e20e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574d065960fa8285d34ea870ee3811a17273cb1b8fc42434e10faed5a2ef5451`

```dockerfile
```

-	Layers:
	-	`sha256:4c293cd5b7c553de33d6a8c461406aced83e3af1d7415c97d139895f4f57ddd0`  
		Last Modified: Wed, 15 Apr 2026 21:33:36 GMT  
		Size: 331.3 KB (331322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:595280f2a9ce1a71f7455b5153eaa12be98428339d123dc88cdb805c118c635f`  
		Last Modified: Wed, 15 Apr 2026 21:33:36 GMT  
		Size: 19.3 KB (19342 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk8-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:a9e88da2f1dd240c2b754d86b7696a9f79cf1d20fdf0f68d5838e913ab1eb037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135108648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24866bc2256118eebf7ea908659f6d1bee2a6d914b48a8b229b348fd2c13f9a`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:20 GMT
ARG version=8.482.08.1
# Wed, 15 Apr 2026 20:23:20 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:20 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:46:24 GMT
CMD ["groovysh"]
# Wed, 15 Apr 2026 21:46:24 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 15 Apr 2026 21:46:24 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 15 Apr 2026 21:46:24 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 15 Apr 2026 21:46:24 GMT
WORKDIR /home/groovy
# Wed, 15 Apr 2026 21:46:24 GMT
ENV GROOVY_VERSION=4.0.30
# Wed, 15 Apr 2026 21:46:37 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 15 Apr 2026 21:46:37 GMT
USER 1000:1000
# Wed, 15 Apr 2026 21:46:37 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d31962388d49f10d3593e394a384b818c01046e78cf4213c87494773368e25`  
		Last Modified: Wed, 15 Apr 2026 20:23:34 GMT  
		Size: 100.6 MB (100563600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e515f9c80ab0442ea232a7d98292971b1f24495dd0c9895685c8450650d68db`  
		Last Modified: Wed, 15 Apr 2026 21:46:45 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1d5958f332a13321dc7936679591b4df5a770bde0479dd1a3e4d0b63910b8c`  
		Last Modified: Wed, 15 Apr 2026 21:46:46 GMT  
		Size: 30.3 MB (30343976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb74250f5d677af4df076b19926c0761a338d6d921adf47d8b6c9973b55b1762`  
		Last Modified: Wed, 15 Apr 2026 21:46:45 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk8-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:f243faebb1e8615ca70947592329e8df13dffd943ff7fdd392f54d7fa75bc6f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 KB (350280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45e37a6dd7076c0fa7a5490d756fc51cb0c46199831efdfcd70cc5eb44a6b40`

```dockerfile
```

-	Layers:
	-	`sha256:cbdf8d256c520ef6a3aad1ebf81654d7048a614708005b51761e0b8ef23b397c`  
		Last Modified: Wed, 15 Apr 2026 21:46:45 GMT  
		Size: 330.8 KB (330804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff2302411f251c77fb6b8c774557c4b024348ed5e2f3aaa8a1c65a60bdd380e6`  
		Last Modified: Wed, 15 Apr 2026 21:46:45 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.in-toto+json
