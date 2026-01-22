## `jetty:11-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:f6d3c3381e494f0fb961819cb39a1e33c8bf1a8cf0e1cf4f030d65ba9c77ddc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:0211eb4938fbc8e86e8435959d1b2af18eed2a33d8b079ed4a3ad1601a7ca92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175989076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc573aee012428bd4a77c51e07b9c706f1042c708eaf68d3b8d9e6f3af67af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:43 GMT
ARG version=17.0.18.8.1
# Wed, 21 Jan 2026 19:00:43 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:43 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:20:24 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 21 Jan 2026 19:20:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:20:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:20:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:20:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:20:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 21 Jan 2026 19:20:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:20:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:20:24 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:20:24 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:20:24 GMT
USER jetty
# Wed, 21 Jan 2026 19:20:24 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:20:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:20:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9893ff21f339b1dac915f0c4f4babba1b9eea3f0737be3f8bc2cf8e11d24c0c`  
		Last Modified: Wed, 21 Jan 2026 19:18:33 GMT  
		Size: 148.4 MB (148367172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b6d70c558e4b29b312e5fc9dfe923a9220790120ea14e9c76f390b65e28cc`  
		Last Modified: Wed, 21 Jan 2026 19:20:34 GMT  
		Size: 23.8 MB (23759923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc77c05cf481d401b62a83ffeae6e944cf155ad79c35c9bcdc8950b59ca203a`  
		Last Modified: Wed, 21 Jan 2026 19:20:33 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5cfb389a1086c95e412fc3eca134f0879dfbed927984c4c5bc37f722150745c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5bf644103a6a76e061119eb8945008077004dd9ff5fcaacab61bdbf41e31aa`

```dockerfile
```

-	Layers:
	-	`sha256:3c5e867d8e88643a8fdb69204091cb4d904fe5e831b79b6d472527967a75d6a1`  
		Last Modified: Wed, 21 Jan 2026 19:20:33 GMT  
		Size: 823.8 KB (823761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b391f49d1aac02d86cf3e672f501d2caca1274fba3848dbfed8ef9d05d8011`  
		Last Modified: Wed, 21 Jan 2026 21:17:32 GMT  
		Size: 17.1 KB (17076 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:337262f21f3cc7d4bbd0fcb831d102858313a05dcb59d18c84dd614fd45cff62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174570859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0268b3c4649cc7faa26c21b931a371b82ded045ecf6abe0977fca645caf1ca6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:59 GMT
ARG version=17.0.18.8.1
# Wed, 21 Jan 2026 19:00:59 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:59 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:20:17 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 21 Jan 2026 19:20:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:20:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:20:17 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:20:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:20:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 21 Jan 2026 19:20:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:20:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:20:17 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:20:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:20:17 GMT
USER jetty
# Wed, 21 Jan 2026 19:20:17 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:20:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:20:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8d87d09c2d3f260e5b0cfb420b36d5fd6729f2919f45b00056a792a16bba98`  
		Last Modified: Wed, 21 Jan 2026 19:01:18 GMT  
		Size: 146.7 MB (146712782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2d4c8035fa84d927435bb947bddae362183e59105c69bc557d1ea7b2641f7`  
		Last Modified: Wed, 21 Jan 2026 19:20:26 GMT  
		Size: 23.7 MB (23660461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c151790be3043b749449a2f5ae235f0f89b0355d1b01716bae18fb1a217e78`  
		Last Modified: Wed, 21 Jan 2026 19:20:23 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0d61a93fdb926d13660b424bf11e895e4c71084746c94bd90ffbc6f4f983de1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.7 KB (839686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9e93a9b8f4b9c326da8ef046a25bfef5144b394d36c194c43255ffbcf5d8df`

```dockerfile
```

-	Layers:
	-	`sha256:86abd919c70a2e9f494d4c17cfcb9152c1a6832922f5279663018367b6b2fea1`  
		Last Modified: Wed, 21 Jan 2026 21:17:37 GMT  
		Size: 822.5 KB (822518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a203f2f652e7f411e5afe57505cb73583f975791a126ac89d923ab143c846585`  
		Last Modified: Wed, 21 Jan 2026 19:20:25 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json
