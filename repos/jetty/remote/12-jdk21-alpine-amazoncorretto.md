## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:9707c57cc412b4a5fcd6b1378dc128a38071c28ca0e6a9f48bef8279502c8bd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:1fb02eb8cbf4d3ac7323eea11057b085165a0d8bb30c44c2bf4664a1583d38cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206098233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37684bfadc7bfb05bc0198ee854369475d6593a7624ba96993c4929ac68cfa25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
ARG version=21.0.7.6.1
# Fri, 04 Apr 2025 01:30:23 GMT
# ARGS: version=21.0.7.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
ENV LANG=C.UTF-8
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_VERSION=12.0.19
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.19/jetty-home-12.0.19.tar.gz
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
WORKDIR /var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
USER jetty
# Fri, 04 Apr 2025 01:30:23 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Apr 2025 01:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e4116f79b2918b726369fcc5f1d66871a9826a9cc697241281621042e8ac1`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 159.0 MB (159033137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88b2b6ea7b9bc82225b70307c988748ca0ff3f47f39a4a006ce51c1d7279570`  
		Last Modified: Wed, 16 Apr 2025 00:08:14 GMT  
		Size: 43.4 MB (43421156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c86ec310a0c637e15b05dda4e030523c7ecb128ae826edc3eb601e82e7ab8d9`  
		Last Modified: Wed, 16 Apr 2025 00:08:13 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c36d71bb8317f7e4a50a0f1871f5630e2476e504f4e539e89d114d2717015b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.6 KB (749594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348aedb8c4a25313c330c4a3b7a6cd621be759bb5d496e43bf495b7ac38c1a4f`

```dockerfile
```

-	Layers:
	-	`sha256:7b58e0e68633f1a41cc7cf303fb739ba364928e1a09ddf89ecbb9952be5b9a16`  
		Last Modified: Wed, 16 Apr 2025 00:08:13 GMT  
		Size: 732.5 KB (732475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ad079cbcd8343534a446e0f9394f66917ed10e18fadac3656874e9744ddf37`  
		Last Modified: Wed, 16 Apr 2025 00:08:13 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:433bd522e0cefb7d11fc3046903037e7b4bb3dfd395b3570394a2db9d9eec686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204314700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1052a7a035523f4115babf2bcdb6de0272e42479804519fc934c2ddd9c049b9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
ARG version=21.0.7.6.1
# Fri, 04 Apr 2025 01:30:23 GMT
# ARGS: version=21.0.7.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
ENV LANG=C.UTF-8
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_VERSION=12.0.19
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.19/jetty-home-12.0.19.tar.gz
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
WORKDIR /var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
USER jetty
# Fri, 04 Apr 2025 01:30:23 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Apr 2025 01:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7555fef64a86b783e2345a5f68fdc874760e3aef8c712ac2699bba1cc222e7d9`  
		Last Modified: Wed, 16 Apr 2025 00:20:33 GMT  
		Size: 157.0 MB (156997903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a800421fbcd867b336f5dd49b1207df76ffd493d853f8b1d60202aa047675b`  
		Last Modified: Wed, 16 Apr 2025 01:14:59 GMT  
		Size: 43.3 MB (43322076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5056c5db8436e3d5ce8eeb483a68440d650826eb911a03e5441e2abf74e0a2`  
		Last Modified: Wed, 16 Apr 2025 01:14:57 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:09beef33697928e0b0076d4436b13db8824ee5ca7d601d170deb86692ea0a9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.1 KB (749093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae67403ec48fa62b45f17e40d4e89888e05419d98b720bb42986f3047a9492`

```dockerfile
```

-	Layers:
	-	`sha256:0ab7093fdc73d37ed1a6af7d6534eaedb4e89c7629b01780d6dcc4810efc87cf`  
		Last Modified: Wed, 16 Apr 2025 01:14:57 GMT  
		Size: 731.9 KB (731882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caecd9fad7e230bbcc548d09f1affe1c1fcc9a61bf710e011fb7b9edc6cc6fdc`  
		Last Modified: Wed, 16 Apr 2025 01:14:57 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json
