## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:116dac5d3c54aa5d4a840288e11b8d764edf443926026c04e721136f1a9a6c92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:8c463083b26c98135d562588daf73098160b37f3e92f10d56d28f89cfba4fa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (206012846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfb57afed0f0d75e03eb3e3ba8155cfed977c0b747476e0c0afc6b9cd831bc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2024 22:29:47 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Wed, 08 May 2024 22:29:47 GMT
CMD ["/bin/sh"]
# Wed, 08 May 2024 22:29:47 GMT
ARG version=21.0.3.9.1
# Wed, 08 May 2024 22:29:47 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Wed, 08 May 2024 22:29:47 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2024 22:29:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c3c30037b360ea1558934aa34c916aa9303537b13bf05accba1f889c8ba6`  
		Last Modified: Thu, 20 Jun 2024 20:47:19 GMT  
		Size: 159.9 MB (159874477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13db514e2c49d5a4fb03a71821e2b7c9b121b1bf264e80c51c30f3164b3f461e`  
		Last Modified: Fri, 28 Jun 2024 20:57:52 GMT  
		Size: 42.7 MB (42719370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5511128707358d789cc6ef283e0f640339481a876f964e5a919337aaf41637bc`  
		Last Modified: Fri, 28 Jun 2024 20:57:51 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5c40fc0fc9f74ff7890dd9df531fcd4f047389c0d8d6009122ca4faa14c4a3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **802.2 KB (802194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7775a5002211336abbaec0bf111a18c5657d07d33586923cbc3a694ba49bac`

```dockerfile
```

-	Layers:
	-	`sha256:85ac0e220a6f1d3edd1fbd753c5a75119b4348433d51011822cd237977b996ba`  
		Last Modified: Fri, 28 Jun 2024 20:57:51 GMT  
		Size: 785.2 KB (785250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f953be97d4299519a5b63df8516bb198c34e68d673e974fb5f073ddded7c706d`  
		Last Modified: Fri, 28 Jun 2024 20:57:51 GMT  
		Size: 16.9 KB (16944 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5dbf854a1dd295d0d951e14440f9e0423bd1d7faa545a71591ba90bfa5d8c830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203523567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae11e6b9207bd198d95edc962675aa7855d4b6586d0649ab0386536d5728b4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2024 22:29:47 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Wed, 08 May 2024 22:29:47 GMT
CMD ["/bin/sh"]
# Wed, 08 May 2024 22:29:47 GMT
ARG version=21.0.3.9.1
# Wed, 08 May 2024 22:29:47 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Wed, 08 May 2024 22:29:47 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2024 22:29:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a2aa088d379d737e12a65d06b983e32465ccd5a65c1f193aa72e5f7b342dae`  
		Last Modified: Wed, 26 Jun 2024 16:54:53 GMT  
		Size: 157.4 MB (157387095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501d34180ba79a4850811477193ef1094b4cceff13cf1ee707a0bea560d4937c`  
		Last Modified: Fri, 28 Jun 2024 21:18:25 GMT  
		Size: 42.8 MB (42777604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17959ae3f831553fa008b339b62ea2cd41e4d7a71f73d6d5c03bfc1de5247212`  
		Last Modified: Fri, 28 Jun 2024 21:18:23 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e00187e1de136d696d4fd0a31f8f5f23b932647a9f32bfd337edb135c01b1371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **801.9 KB (801901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df14382a3a71eaf8279fe2a0db90e110b4c113d6354cd60a77cfb1e60b2c4a0`

```dockerfile
```

-	Layers:
	-	`sha256:bb728c27767b8a88d4de9116a5cae65916dc6adf4e4cf95c41a5ca642179ae85`  
		Last Modified: Fri, 28 Jun 2024 21:18:23 GMT  
		Size: 784.7 KB (784656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcafc154b0ed95cbd89d507eb982399c02385f8e716868854dac25f919048ce`  
		Last Modified: Fri, 28 Jun 2024 21:18:23 GMT  
		Size: 17.2 KB (17245 bytes)  
		MIME: application/vnd.in-toto+json
