## `jetty:12-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:cdfd7864234591744d8c51cbac4f78068c5f9f1372d1d2645565a511b26f1c30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:92372e0147f4e5a251f7bd83175dd6d37eb01c8af0f0f592e59120c3adbcd094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207510545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1057defefa115a98df04aead4ec4124b7fe3a28ba4ee6020ff586b3a03e4da5b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:25 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:25 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:25 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 06 May 2026 17:07:54 GMT
ENV JETTY_VERSION=12.1.9
# Wed, 06 May 2026 17:07:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 06 May 2026 17:07:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 06 May 2026 17:07:54 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 06 May 2026 17:07:54 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 06 May 2026 17:07:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Wed, 06 May 2026 17:07:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 06 May 2026 17:07:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 06 May 2026 17:07:54 GMT
WORKDIR /var/lib/jetty
# Wed, 06 May 2026 17:07:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 06 May 2026 17:07:54 GMT
USER jetty
# Wed, 06 May 2026 17:07:54 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 17:07:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 May 2026 17:07:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70996f4731d80bb777dc007c01bbb313c2d7205086bed0275a9259be9c42ec88`  
		Last Modified: Wed, 22 Apr 2026 21:34:41 GMT  
		Size: 148.6 MB (148583454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7450f6af9b2ef5f03947e30e9727bf9f1b5bfd933caa91d5a6640b7b7ef5522c`  
		Last Modified: Wed, 06 May 2026 17:08:05 GMT  
		Size: 55.1 MB (55061026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a0a1251679e8b610d26e39ae8f3519b2d0b9c8bb00ef6626fcd931414b14c3`  
		Last Modified: Wed, 06 May 2026 17:08:03 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:299ce8be410a6cc868d533364f3c437910dd2295df185ae9a2065c6adf3b6384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1031263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d43935337e6c33ad2f332afd7458159e02a95bde9b1791a4f3c01dfbb5c0373`

```dockerfile
```

-	Layers:
	-	`sha256:47a18b6077dffcb12d248047c6ba7326ca220a530a2700d0e90f0b9431dd14e0`  
		Last Modified: Wed, 06 May 2026 17:08:03 GMT  
		Size: 1.0 MB (1014193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a699fe5789e05c26f6d065dc563bc4360b96878be91b1d20c8166072727270b`  
		Last Modified: Wed, 06 May 2026 17:08:03 GMT  
		Size: 17.1 KB (17070 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2d07700d570efef7461dac8e30adf29db49c2e82d57654fefac1af16e524cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206100079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2f38e59b58cf48405f38bf8014a8b6cf315cee704250c69cdffbc81c6c1ec4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:22 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:22 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 06 May 2026 17:07:44 GMT
ENV JETTY_VERSION=12.1.9
# Wed, 06 May 2026 17:07:44 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 06 May 2026 17:07:44 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 06 May 2026 17:07:44 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 06 May 2026 17:07:44 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 06 May 2026 17:07:44 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Wed, 06 May 2026 17:07:44 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 06 May 2026 17:07:44 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 06 May 2026 17:07:44 GMT
WORKDIR /var/lib/jetty
# Wed, 06 May 2026 17:07:44 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 06 May 2026 17:07:44 GMT
USER jetty
# Wed, 06 May 2026 17:07:44 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 17:07:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 May 2026 17:07:44 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529315e3631a56927dc9186f923e06f688e00895e152f54e0716f3971048783`  
		Last Modified: Wed, 22 Apr 2026 21:34:43 GMT  
		Size: 146.9 MB (146937643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dca8528491568c946ea00beae08c501016d560220da6755ac0116ad20f1a620`  
		Last Modified: Wed, 06 May 2026 17:07:55 GMT  
		Size: 55.0 MB (54960689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267d2e515d9b00f775ce153d85c424f78738f4d1727252d5ce85a0bc9e6db4f9`  
		Last Modified: Wed, 06 May 2026 17:07:54 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ac078c949145a28f77645de697076a2ccdc74835ca9e83b2729caac775caf68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1030112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5a6b82960d19235bf015a943d718ca613f7a6936029e112b8cc58504639242`

```dockerfile
```

-	Layers:
	-	`sha256:7935a944746e292d80110e50ca720055dcbdbb247746da7e322513c0859e4bb7`  
		Last Modified: Wed, 06 May 2026 17:07:54 GMT  
		Size: 1.0 MB (1012950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8baa4892d9275bd3690687cdafe1544094ee393ca3d2dcdb9620bcafb3030a2`  
		Last Modified: Wed, 06 May 2026 17:07:54 GMT  
		Size: 17.2 KB (17162 bytes)  
		MIME: application/vnd.in-toto+json
