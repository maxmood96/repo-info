## `jetty:12-jdk25-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:75c6f94681b1d92727de295acc648dd83c102da78bf38e74624cbbe645f51e9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk25-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:2d3b8b040f631c9d15f1a1b3528f6fe98f1c53e0b58a12ea62de82676e2ecb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239690852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ce3f88366a5910fd544288c4d2e9008c2debf5c779312b1401775cae3ae0d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:33 GMT
ARG version=25.0.2.10.1
# Wed, 15 Apr 2026 20:24:33 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:33 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:24:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:34:49 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 15 Apr 2026 21:34:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Apr 2026 21:34:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Apr 2026 21:34:49 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Apr 2026 21:34:49 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:34:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 15 Apr 2026 21:34:49 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 15 Apr 2026 21:34:49 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 15 Apr 2026 21:34:50 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Apr 2026 21:34:50 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 15 Apr 2026 21:34:50 GMT
USER jetty
# Wed, 15 Apr 2026 21:34:50 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:34:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:34:50 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f961561d31cd5037ff5298d6237cb82f4e652e35bbe8021a675c623cdeb1b35`  
		Last Modified: Wed, 15 Apr 2026 20:24:54 GMT  
		Size: 180.8 MB (180759200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba0b070fd3d24b4bb2cc940097c44449ac74bf513692b8670b4d26e1d6b62f`  
		Last Modified: Wed, 15 Apr 2026 21:35:03 GMT  
		Size: 55.1 MB (55065587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf62d9eaf780632c967af8f543502ceae98dececdd887fd60a7e95b84c53d03`  
		Last Modified: Wed, 15 Apr 2026 21:34:52 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1efd7e59dff25eb98098e713593b2a9079210275636aa34b136b922110a88aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1069987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac1358a6f99109166944a21ab077c4e40a909041b01e20b4060a01c191e1812`

```dockerfile
```

-	Layers:
	-	`sha256:16c5b13f92df8ad96b5e7dae628ff4d571ff9a74d219ad0b93b34f73a329dc1f`  
		Last Modified: Wed, 15 Apr 2026 21:35:01 GMT  
		Size: 1.1 MB (1052916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897f35ba0a8c4802ce7e933e1a4eb2baa6e0d57e7c8ce6acd5417121be5245c6`  
		Last Modified: Wed, 15 Apr 2026 21:35:01 GMT  
		Size: 17.1 KB (17071 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk25-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a1a587bca12465f3470a10d0ffa7f43185d816be24ede2e14bd9099dcac0c8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237577853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050785ff0a9668c3b322b23231358e01771805bdf8902e886d98214681dee479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:59 GMT
ARG version=25.0.2.10.1
# Wed, 15 Apr 2026 20:23:59 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:59 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:47:33 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 15 Apr 2026 21:47:33 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Apr 2026 21:47:33 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Apr 2026 21:47:33 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Apr 2026 21:47:33 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 21:47:33 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 15 Apr 2026 21:47:33 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 15 Apr 2026 21:47:33 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 15 Apr 2026 21:47:33 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Apr 2026 21:47:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 15 Apr 2026 21:47:34 GMT
USER jetty
# Wed, 15 Apr 2026 21:47:34 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:47:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:47:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d751edfe3e5205eea6210b418197b25f4c7c31b99665652de330dfd754bd47`  
		Last Modified: Wed, 15 Apr 2026 20:24:26 GMT  
		Size: 178.4 MB (178411940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f68bdf07e04e286e1bd992e8d991720dcb7f9366256e552cffb52920ae5fff`  
		Last Modified: Wed, 15 Apr 2026 21:47:46 GMT  
		Size: 55.0 MB (54964167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956d4a66bf267e424f3e21228221f188f85fd35b77f0e4b0336e174c46283516`  
		Last Modified: Wed, 15 Apr 2026 21:47:44 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:2c365c89b9c5e2060b0fa857b118fa3eda6d1e09a5fe4b78fb2f3c8307b57248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1068832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4a44ef827e1b91ea938ed622551e546ff9b4982e69b8e9f14dc3f63bbda92d`

```dockerfile
```

-	Layers:
	-	`sha256:f00fb22178e281a15fd4fc4d490c9fc7a224d3a1c365662512a3e5360d5f4c9d`  
		Last Modified: Wed, 15 Apr 2026 21:47:44 GMT  
		Size: 1.1 MB (1051670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d021c84c0828768d6c93cf2774f8e95f6a18f2a85795c082f8f160edeb3e1c`  
		Last Modified: Wed, 15 Apr 2026 21:47:44 GMT  
		Size: 17.2 KB (17162 bytes)  
		MIME: application/vnd.in-toto+json
