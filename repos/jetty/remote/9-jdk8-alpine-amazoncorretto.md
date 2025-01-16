## `jetty:9-jdk8-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:fb88957b23a6480462e2805025ce12f965094f5fb4e26269ec70743bfd16718d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk8-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:1e0915752f7110778edfba6a44d5a00d311e7b1ebf93fc310fc2d6c4e618882b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122930423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f375184611835c1e16bfd8f0b41f44c64c66811a5856d9c19042b75da576f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
WORKDIR /var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
USER jetty
# Tue, 14 Jan 2025 05:07:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a15a91bb85d85949856ba1d3ccade006b10de18ccdc8675614554939053055`  
		Last Modified: Wed, 08 Jan 2025 18:09:49 GMT  
		Size: 100.2 MB (100195138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04e1e4737b3dc418a60f3705ca39ec1da9ab34a70b1a33f864d96772c786bb2`  
		Last Modified: Wed, 15 Jan 2025 20:29:13 GMT  
		Size: 19.1 MB (19107335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc395de6c5279929d8ca6b26f7491ef1735c67e1737e2ea17e3114cb9838506`  
		Last Modified: Wed, 15 Jan 2025 20:29:12 GMT  
		Size: 1.7 KB (1658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:6643f9b2bc5b945d19c6d412b1f63712af4a3620a225e541321d6280e665e9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 KB (579121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc616e4ff606478d06e2df877fed9c847d3d103a546ed00b9e34f276c95d3e17`

```dockerfile
```

-	Layers:
	-	`sha256:7dca5c4a364f075db07193264c2613d1aca0855c4ec670d85825345c2944ec34`  
		Last Modified: Wed, 15 Jan 2025 20:29:12 GMT  
		Size: 562.0 KB (561982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b66cef81ec541b37ae25bf4ef915b3226d65b577764c1d799166aa3c6c12cf`  
		Last Modified: Wed, 15 Jan 2025 20:29:12 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk8-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1fd45de3de77516d641a147ea4c10a8fec79fe17b1c1535ed0bf591489ec9192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123230122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09de92e993c6aaafc8c691c4c8680bc1220bebb48f259b88524f1ecc1cd47466`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
WORKDIR /var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
USER jetty
# Tue, 14 Jan 2025 05:07:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d676acef0262114b575dbe155e1594d5a6f3b4a62c043566b36b1d8e6a050b5c`  
		Last Modified: Wed, 08 Jan 2025 22:17:27 GMT  
		Size: 100.0 MB (99978735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274aabbf5336bf7d7898bb2e97b3237ecf47901ea71e7842ff35315925745b1a`  
		Last Modified: Wed, 15 Jan 2025 21:07:11 GMT  
		Size: 19.2 MB (19158926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab50315906336d04b8145b4f2063861bc06bb182e511526aadd94043fb84e6`  
		Last Modified: Wed, 15 Jan 2025 21:07:10 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b0587d83fabf490a2905c5e75864fe738be845d85281635ee5881613972bf99f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.3 KB (579329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4caf7ad8da50168323f75f4530aea0d9c7aa4b05924ab5d05cd3a415c8470db`

```dockerfile
```

-	Layers:
	-	`sha256:4685ae2670acb2b3d1e1c6789abfa200b1dacc2fdf3a78c6904f4c35e64b6932`  
		Last Modified: Wed, 15 Jan 2025 21:07:10 GMT  
		Size: 562.1 KB (562102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e944f151e67cc0d12860845c6acb2798cdec1d2db897f77e5ffb5c46d1b771c5`  
		Last Modified: Wed, 15 Jan 2025 21:07:10 GMT  
		Size: 17.2 KB (17227 bytes)  
		MIME: application/vnd.in-toto+json
