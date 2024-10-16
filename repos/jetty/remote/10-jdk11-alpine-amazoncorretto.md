## `jetty:10-jdk11-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:a6963e4f24cb284d6b5c029d8418b316819e5822c9b89d54f54de1d98cf5a9d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk11-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:24dd1a56e7f3dac865c4956d2a2b98d155bd73d981d1314fde2721291191abc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165471295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5125476ff6826b1d31b81fc6d976d67dae89539467ebd8ce7815ff8a5c103f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
ARG version=11.0.25.9.1
# Tue, 10 Sep 2024 00:22:25 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
ENV LANG=C.UTF-8
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_VERSION=10.0.24
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.24/jetty-home-10.0.24.tar.gz
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
USER jetty
# Tue, 10 Sep 2024 00:22:25 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Sep 2024 00:22:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e37f65f08727562421b90179a5bc71a9db33e28fb6e68c95b4a998e1643d76f`  
		Last Modified: Wed, 16 Oct 2024 17:56:12 GMT  
		Size: 141.9 MB (141908598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0098234ecdff3c38d15cc0dd2829899f2d38df1f85b75870c00b26f80db23`  
		Last Modified: Wed, 16 Oct 2024 19:00:31 GMT  
		Size: 19.9 MB (19937224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00870d73970d18607d3bde5e6d8aa056173d9cad3fe323380efaedc16f9fd843`  
		Last Modified: Wed, 16 Oct 2024 19:00:31 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:a6fd0d05032f87d42212ae3c6b37ed4c5531ff186ed91823b83102fd3078a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.5 KB (732464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59889e62f6d6d1e8d43d3da295f9ae8483fd300bcc3add9d86ba60b96187be9b`

```dockerfile
```

-	Layers:
	-	`sha256:7cf3cd11d8113f4a99c324125de96fc74a88e9dc087a01deea9ac85531879ebd`  
		Last Modified: Wed, 16 Oct 2024 19:00:31 GMT  
		Size: 715.3 KB (715341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a1c46bd1df9aca6b0a12d84c6fe448e9add14d5e74f25a4a8be46a8440ff53`  
		Last Modified: Wed, 16 Oct 2024 19:00:30 GMT  
		Size: 17.1 KB (17123 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk11-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:05ae8aaa2866659736fc4aef945f07c86fc3182652cb7f1607b75f3f13bb1290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164109149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b301173d61024d7f1007290fd4585243979072d048cc2cff38f305ba4b7d86c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
ARG version=11.0.25.9.1
# Tue, 10 Sep 2024 00:22:25 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
ENV LANG=C.UTF-8
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_VERSION=10.0.24
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.24/jetty-home-10.0.24.tar.gz
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
USER jetty
# Tue, 10 Sep 2024 00:22:25 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Sep 2024 00:22:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d75e0b84f6a291f6a433e35e083f59f3d0af9f4e372a4ba452f6ad81e4ab3e`  
		Last Modified: Wed, 16 Oct 2024 18:19:12 GMT  
		Size: 140.0 MB (140030791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46e3ca2b7446e286e4147d8450456153298d48467afd14bbed2f9203846c57f`  
		Last Modified: Wed, 16 Oct 2024 20:11:17 GMT  
		Size: 20.0 MB (19989046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6086bb5c74b4f1c4b9d409dcfcfe131be489d07f5dbb17157d16108f6470b542`  
		Last Modified: Wed, 16 Oct 2024 20:11:16 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:67fb6ff576678dd426892676acb86be5e4d6fac43b8579386bd24ae275329fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.6 KB (732624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac886433b1b90a2ee7c76e371d792d47ad049c4ec9461b241c2d25a548122ea`

```dockerfile
```

-	Layers:
	-	`sha256:e57969f1d8c02dd45f921ccba85cbd8925e42a2e566eac926906c175bf55acde`  
		Last Modified: Wed, 16 Oct 2024 20:11:16 GMT  
		Size: 715.4 KB (715385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41c7b58a87a263eb34048ec0534487ac253900fad0d97d1d67b4ed5fb62c702`  
		Last Modified: Wed, 16 Oct 2024 20:11:16 GMT  
		Size: 17.2 KB (17239 bytes)  
		MIME: application/vnd.in-toto+json
