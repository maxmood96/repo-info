## `jetty:9-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:3aa21a68b2772928603d7d46d4931d604c3c4f076793412d8393446733f8a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:ede2d2f94e9f95f19deab5275868622017ef043e903c80f8fcbf645564cfb98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167954712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1dd2da2123893b329967eba1ee8436b26755409a41bf08ed773fe8fc6e1d84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
ARG version=17.0.11.9.1
# Fri, 15 Mar 2024 05:21:34 GMT
# ARGS: version=17.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0db5f63c3906482ac90304cf0e89c91fc810984dd49f92dd3a9d8ab4b99878b`  
		Last Modified: Fri, 05 Jul 2024 19:56:32 GMT  
		Size: 146.2 MB (146235770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b21e54968d39698e95c1589063c3bf199f6fa7f510c0387aa6ae690814be7`  
		Last Modified: Fri, 05 Jul 2024 20:51:43 GMT  
		Size: 18.3 MB (18299944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fa7de8730958a2bd4c98bab812e601c73e3d4ec0be9dbff633b96cb99d0ec0`  
		Last Modified: Fri, 05 Jul 2024 20:51:42 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3e2a0e7d18ca9b0e7add9da486bb6232da3f1d103fb1dac8a79d61e0e5833119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.5 KB (691501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794a734cc5449c2db2e935306fe8f4b5d38742d750febbcba05d2b42443bbf13`

```dockerfile
```

-	Layers:
	-	`sha256:3974605d3863c68d53efa66028e3f5d01d3bfa7cc57e8939db205f2522d046f5`  
		Last Modified: Fri, 05 Jul 2024 20:51:43 GMT  
		Size: 674.4 KB (674386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44772399a18291b2ccaa3914e262e00b4d0e855f28d4beba92079c4936d80680`  
		Last Modified: Fri, 05 Jul 2024 20:51:43 GMT  
		Size: 17.1 KB (17115 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:977191bc6c2933b770b4b429e5c8cd9f5fcb9ec0adeb6e1bb8ac43ebe536729b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166013006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff48587d9cf997ff7a859448cd6b6e641a4c5d2a7fb6844c3b89bef5526428f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
ARG version=17.0.11.9.1
# Fri, 15 Mar 2024 05:21:34 GMT
# ARGS: version=17.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7718162609e58e530ed10c8d6174f115f955dcfba9f4ca76240996a7ba3ba0`  
		Last Modified: Fri, 05 Jul 2024 20:19:41 GMT  
		Size: 144.3 MB (144295392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c229cc7a5d8ce16171608f267688860f32530223eeb165bd0c838e2b2e4b441`  
		Last Modified: Fri, 05 Jul 2024 20:56:45 GMT  
		Size: 18.4 MB (18358745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be81520205bfb4f51a1594e58d53941912969bbfead61b2cc59bada2565b08e8`  
		Last Modified: Fri, 05 Jul 2024 20:56:44 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:90200d09b51ed5d9f8e5a50fa49e55d2d3fff7cdde39db01d7255b7cf226d97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4acec4459a0ca5d904c3ac339ad3cb13d67a19568fece96c6fbeac482331f34`

```dockerfile
```

-	Layers:
	-	`sha256:9a7028f00d297d34321a0710bbf41b79e40d8abdc3e7aa3ad61236de832b73fb`  
		Last Modified: Fri, 05 Jul 2024 20:56:44 GMT  
		Size: 673.8 KB (673792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e468158ed851dee4692cadfbc8dd7f3c57b48c9bca9b9693f7248f1bfb47ff65`  
		Last Modified: Fri, 05 Jul 2024 20:56:44 GMT  
		Size: 17.5 KB (17512 bytes)  
		MIME: application/vnd.in-toto+json
