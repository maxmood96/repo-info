## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:9c29545a3bb3daf279ebabee05d5c765f1d55b92c300dd7e3f07ac58c9a8d256
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4836b68d94a2d47ee02ef6c9ff3c60d007aefee01cc9f692807ea8f2b45d4610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220521342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae3958fbf609da6418dc6aa2a6aafbceec9d358fb50ce88a940d52068349033`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:20 GMT
ARG version=21.0.10.7.1
# Wed, 15 Apr 2026 20:16:20 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:16:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:34:56 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 15 Apr 2026 21:34:56 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Apr 2026 21:34:56 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Apr 2026 21:34:56 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Apr 2026 21:34:56 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:34:56 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 15 Apr 2026 21:34:56 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 15 Apr 2026 21:34:56 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 15 Apr 2026 21:34:56 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Apr 2026 21:34:56 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 15 Apr 2026 21:34:56 GMT
USER jetty
# Wed, 15 Apr 2026 21:34:56 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:34:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:34:56 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71448d6e675e667655615378e72942f52abaf0b0bca7c6602dc0fbe187e2c587`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 161.6 MB (161590450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ab54dd77169c21d2f43d9be3d3a40616bdb78ea7cd3a01ea9aa530c01f00e7`  
		Last Modified: Wed, 15 Apr 2026 21:35:07 GMT  
		Size: 55.1 MB (55064827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077e47278054aa73c55acc9001a537218d79f64d70f781821520441883e132a9`  
		Last Modified: Wed, 15 Apr 2026 21:35:06 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5b2abc362f07b362fd0f4f78530540b86bd3651b489e6b30ea5c90da06d1ba31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961fff238a1467814afb0cf6a6cfcf7ea28c3cb554230b4099637f3d1a4ea41f`

```dockerfile
```

-	Layers:
	-	`sha256:1f86b20933fd7a80b87a45be1e88ebfd36b9e988d2d6b16fc578903e83a03c8c`  
		Last Modified: Wed, 15 Apr 2026 21:35:06 GMT  
		Size: 1.0 MB (1043816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb343c7e172c8921ece702ac569cf5ac85eb4735976f0c10d5bfc2898fe56665`  
		Last Modified: Wed, 15 Apr 2026 21:35:06 GMT  
		Size: 17.1 KB (17071 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e35498008a7ac71a4b2689f3b8e0828daf9457609187b7fe2f0e2b8b78d92d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218781465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02a52443df318258fdbed6fb6b2f26dc0d2b579b2c7716d341ed3cefa8f549b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:46 GMT
ARG version=21.0.10.7.1
# Wed, 15 Apr 2026 20:23:46 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:47:36 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 15 Apr 2026 21:47:36 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Apr 2026 21:47:36 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Apr 2026 21:47:36 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Apr 2026 21:47:36 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:47:36 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 15 Apr 2026 21:47:36 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 15 Apr 2026 21:47:36 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 15 Apr 2026 21:47:36 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Apr 2026 21:47:36 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 15 Apr 2026 21:47:36 GMT
USER jetty
# Wed, 15 Apr 2026 21:47:36 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:47:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:47:36 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1cf2342851f77ea9f415795ed3cd8dada823b419d754c75ab485a6a7a59996`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 159.6 MB (159615722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eacf47c3b53a6433dcf8d0beaf6bada8d622fedaa0b0e0b75ae65adda2b329`  
		Last Modified: Wed, 15 Apr 2026 21:47:47 GMT  
		Size: 55.0 MB (54963997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6837a342da55cf90283a53e87a7467deccf3e62202e2f118bbcbc487b29d12ca`  
		Last Modified: Wed, 15 Apr 2026 21:47:46 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:17856a92319fe7469b0b49388526c358d0edfe6a35657426fb02c9ca5880dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118157a252f0140685c06224082cd2905b48575e08c72aa79ba721df11c0059a`

```dockerfile
```

-	Layers:
	-	`sha256:626bf6e6199369fb4ac3d1de0e0ee62f0b8e1edb9ac3f20326d3450cc1d8e749`  
		Last Modified: Wed, 15 Apr 2026 21:47:46 GMT  
		Size: 1.0 MB (1042573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c4a689fca86fac34c001964a2c17010b69144b0cf76ccb4093eee628df3af3`  
		Last Modified: Wed, 15 Apr 2026 21:47:46 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json
