## `jetty:9-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:e78bdc0ee4972c071ab406391d1eaa901cafce896ba71fac735835ae366d57ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:3c1011131f736f82e0502e9a2178845273cb2e3eedb9939020b485c9c51ca3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171665177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289f33f6a078015551f0d16d0727b35957ca3c479de658fb87f68e0f9058afb4`
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
# Wed, 21 Jan 2026 19:18:43 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Wed, 21 Jan 2026 19:18:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:18:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:18:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:18:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:18:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Wed, 21 Jan 2026 19:18:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:18:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:18:43 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:18:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:18:43 GMT
USER jetty
# Wed, 21 Jan 2026 19:18:43 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:18:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:18:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9893ff21f339b1dac915f0c4f4babba1b9eea3f0737be3f8bc2cf8e11d24c0c`  
		Last Modified: Wed, 21 Jan 2026 19:18:33 GMT  
		Size: 148.4 MB (148367172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafbe39b40c153f8c5bddfc7c9544bdee7c182490ab0cabc9064bbecbb151139`  
		Last Modified: Wed, 21 Jan 2026 19:18:53 GMT  
		Size: 19.4 MB (19436025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94264e2c9e9e6dbe98df8bc6c0c9d65c050eea3e6b17a4178dd2a250d776be23`  
		Last Modified: Wed, 21 Jan 2026 19:18:52 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:36bef0ffbbe73b06d21e69abe93640f39b7eb03ad4ffa8952893b83f51f8d636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.6 KB (826578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8338d2ef31dbbf6092a8dc3fd2c89b72e40dab7dcd87ff6a961125b477d47a1`

```dockerfile
```

-	Layers:
	-	`sha256:579adef661538bc3a9ddcc3c575e85210bfafacd0461307659c3c5c182f27ffc`  
		Last Modified: Wed, 21 Jan 2026 19:18:52 GMT  
		Size: 809.5 KB (809472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaab1497a2ed7a67df1f1093aaace0167f3182afdefaf9012891642358f74fc8`  
		Last Modified: Wed, 21 Jan 2026 19:18:52 GMT  
		Size: 17.1 KB (17106 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e211d0d35300a9144a18705e7304b44c2872b6858df5c9501aeee5bfe1c5e276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170245200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9fe5974ecc86a6f653adc6e24afa7be573bb21805d4c55120eb884e8cea40`
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
# Wed, 21 Jan 2026 19:16:52 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Wed, 21 Jan 2026 19:16:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:16:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:16:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:16:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:16:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Wed, 21 Jan 2026 19:16:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:16:52 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:16:52 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:16:52 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:16:52 GMT
USER jetty
# Wed, 21 Jan 2026 19:16:52 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:16:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:16:52 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8d87d09c2d3f260e5b0cfb420b36d5fd6729f2919f45b00056a792a16bba98`  
		Last Modified: Wed, 21 Jan 2026 19:19:15 GMT  
		Size: 146.7 MB (146712782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a9b551be5d31395dc7bfcb056507d6bcdc8392bfdfd40ec1028af40775cd3`  
		Last Modified: Thu, 22 Jan 2026 11:04:12 GMT  
		Size: 19.3 MB (19334803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9848d0aa62d1280b8b6de9ea23b8fbf14cc974ab77c39c11238ca2cabb355aef`  
		Last Modified: Wed, 21 Jan 2026 19:17:01 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c179580f2dde1b95f07845fd409397a108ff2e7112ea508a841502404fd03899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.4 KB (825427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcbf76da2e8e1d9dc03144f9061371889b0de0d8a196aa212517533cf693baa`

```dockerfile
```

-	Layers:
	-	`sha256:ca826202e9bc424f283f7ff6744b7922c98966a993dc4be0a457a6ee9db88ae8`  
		Last Modified: Wed, 21 Jan 2026 19:17:01 GMT  
		Size: 808.2 KB (808229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c0204c26215c4e2cfe7dea31eddf6378b0cd9fbd9960320ffd98fb22f50a3a`  
		Last Modified: Wed, 21 Jan 2026 19:17:01 GMT  
		Size: 17.2 KB (17198 bytes)  
		MIME: application/vnd.in-toto+json
