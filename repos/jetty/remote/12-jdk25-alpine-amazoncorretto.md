## `jetty:12-jdk25-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:b59c1e52397448e43ecde150426c2b3156f25d3ada54491df39b09e276b9bcf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk25-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:bba4dd150dcc69ddf92c6b81728d84ea20dd6b506a0a432326a23170e242f1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239935053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fd34746aafea2525a85c7f5a652a6ec112c43c557f3d9656a6dd1f5cd16592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:59 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:52:59 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:52:59 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:52:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:52:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 10 Mar 2026 16:40:16 GMT
ENV JETTY_VERSION=12.1.7
# Tue, 10 Mar 2026 16:40:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2026 16:40:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2026 16:40:16 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2026 16:40:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 10 Mar 2026 16:40:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.7/jetty-home-12.1.7.tar.gz
# Tue, 10 Mar 2026 16:40:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Mar 2026 16:40:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Mar 2026 16:40:16 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2026 16:40:16 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Mar 2026 16:40:16 GMT
USER jetty
# Tue, 10 Mar 2026 16:40:16 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Mar 2026 16:40:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 16:40:16 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce024e0c1fc281f3f61f3cf3a1e72dcd0c8f1a01d7b36ccd799f9d0d0de6c041`  
		Last Modified: Wed, 28 Jan 2026 02:53:20 GMT  
		Size: 180.8 MB (180759289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d6a7324e4f604450c50cb6bb1643fa18db150d81ca37ad3d95caffef4fca22`  
		Last Modified: Tue, 10 Mar 2026 16:40:28 GMT  
		Size: 55.3 MB (55312067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1458acd38aeee464e9b2abde35385ac78ec4d88c9c37c9e25ebf85c0057fb731`  
		Last Modified: Tue, 10 Mar 2026 16:40:27 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e58d6bb260ac2ac869c77f3fead1f9ccd764032870aa471c5278c73274080759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1072861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34da5537ab0d5354aee0b117158f4ee83dc7ec92938516c141805adb17eef64c`

```dockerfile
```

-	Layers:
	-	`sha256:e6894eaa7bb99fbb3bf96fd41920bc0baffa3fffffc6fa926d6b8eb746dcfe84`  
		Last Modified: Tue, 10 Mar 2026 16:40:27 GMT  
		Size: 1.1 MB (1055790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d2a31a6cb2d302f5c4d7f77ae70cfa34ecf7d05f16f7d737f5775cb6c75d14`  
		Last Modified: Tue, 10 Mar 2026 16:40:27 GMT  
		Size: 17.1 KB (17071 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk25-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:387a469fe8af45f4b4ddc27c308f30d82fae3937815dddcea94db7b71e01b588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237823544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501e9104909f4ba9cbac0259b57d0d0bda738c3e611724c73367db217be0d74e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:31 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:54:31 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:54:31 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:54:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:54:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 10 Mar 2026 16:39:11 GMT
ENV JETTY_VERSION=12.1.7
# Tue, 10 Mar 2026 16:39:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2026 16:39:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2026 16:39:11 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2026 16:39:11 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 10 Mar 2026 16:39:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.7/jetty-home-12.1.7.tar.gz
# Tue, 10 Mar 2026 16:39:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Mar 2026 16:39:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Mar 2026 16:39:11 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2026 16:39:11 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Mar 2026 16:39:11 GMT
USER jetty
# Tue, 10 Mar 2026 16:39:11 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Mar 2026 16:39:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 16:39:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea00285b52f6f6c9e088cd08bc54a41499c353ac64712efcaf2aff682f021f1a`  
		Last Modified: Wed, 28 Jan 2026 02:54:52 GMT  
		Size: 178.4 MB (178412260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48239bda77823d41686785a64614d2011b26844a7e5ad26e4fd283f1093882b3`  
		Last Modified: Tue, 10 Mar 2026 16:39:22 GMT  
		Size: 55.2 MB (55212317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4b79c2773799ab978c053ef887a37b43e789ae71ed463914ee856321d87ca`  
		Last Modified: Tue, 10 Mar 2026 16:39:21 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e0026445df4581226637a7a66a61305389cd5f44e611a85c6a33184c8a12a515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c536cdb5f7b013e39d360f2b125afadc6f630dd87986fd84fda617ec00162555`

```dockerfile
```

-	Layers:
	-	`sha256:e5923b0e42213cde695aabcd4c794587bbb5a027b0708e424923affa199de9ff`  
		Last Modified: Tue, 10 Mar 2026 16:39:21 GMT  
		Size: 1.1 MB (1054544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46f319cd53454177f6425c7cb3fe7c2ea83eadca8b05699c1acfadef467b4dd`  
		Last Modified: Tue, 10 Mar 2026 16:39:21 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json
