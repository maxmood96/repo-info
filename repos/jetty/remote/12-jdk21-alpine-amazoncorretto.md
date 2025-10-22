## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:a8e4790c8c864bb1914054e6308c118813811ead4b94a3eded6d3c1a4a4d2d09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:02cf5b3061393b6c822017415872797108c88f5b1a6d32d2db2ea4ef59dd492f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 MB (220309329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898fa9471f9685f9ae7d6f1b050de129297c566d9d605522d9ce7264da92e723`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_VERSION=12.1.3
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 22 Oct 2025 00:53:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 22 Oct 2025 00:53:34 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 22 Oct 2025 00:53:34 GMT
USER jetty
# Wed, 22 Oct 2025 00:53:34 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 22 Oct 2025 00:53:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Oct 2025 00:53:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0232a5c1ec36753528564a0c37c51dd325df2a291ba8a36a4d16515714648b`  
		Last Modified: Wed, 22 Oct 2025 00:52:18 GMT  
		Size: 161.6 MB (161577544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555e14da125b9ff6e66c957c62e4392213ea0301e4151de1cf56099f0a6602a7`  
		Last Modified: Wed, 22 Oct 2025 17:46:26 GMT  
		Size: 54.9 MB (54927457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b62cc352cd214264758a98e053c1cf6c5586b21644edb6ba6159d9f7655a84b`  
		Last Modified: Wed, 22 Oct 2025 17:46:14 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8a5374a91d16fef45d05e9cb6c229ef6ba4af479eae5a24ca2df67108f5bf9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bf40f5b1682bc062d73d6cb976bea3a8298bd11fa19402ffa8bc0b096b5d68`

```dockerfile
```

-	Layers:
	-	`sha256:b82f3ded4f44e0dd681ed0325a7a4ca7f41710c334338b75308993eb1ab11813`  
		Last Modified: Wed, 22 Oct 2025 20:17:33 GMT  
		Size: 1.0 MB (1046319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d99ac781f31cb6ddceb3a344482dba9b90533608824486faae1d019308ef5d6`  
		Last Modified: Wed, 22 Oct 2025 20:17:34 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:96a582902a2e117ff2cdf1caf98cefbdf6233e93fc15f45bc2db65df9bf1550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218570476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a506bbd23bd34c6d0a067def17f7f631f638755bb2189f3af186d6f24001cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_VERSION=12.1.3
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 22 Oct 2025 00:53:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 22 Oct 2025 00:53:34 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 22 Oct 2025 00:53:34 GMT
USER jetty
# Wed, 22 Oct 2025 00:53:34 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 22 Oct 2025 00:53:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Oct 2025 00:53:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd998d4c35c3887cf9b7d0f274f70b8cae4a0a1bcf69e39670164930f639106`  
		Last Modified: Tue, 21 Oct 2025 22:13:22 GMT  
		Size: 159.6 MB (159595117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e7ef6820f86440323e1ebf14d76eadc4c0949af6fab45d38de077bb618e24`  
		Last Modified: Wed, 22 Oct 2025 17:46:31 GMT  
		Size: 54.8 MB (54835414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83607de6dc89129c0d7bbc42ccc5ed2a22582013cbd04f627d73a0a500a6f0a1`  
		Last Modified: Wed, 22 Oct 2025 17:46:26 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b80e888f07b93a917d20d141908ffbcc194f1cd38f3bcda8aee3a3f7410f207f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c47785263b4c238000b5d9a809b4c77845b49a9ebfbdb8805489c24542f29b7`

```dockerfile
```

-	Layers:
	-	`sha256:dcc85a9d5495bb0f4865e9591dfeec985f48890585a2fa69f519f5b9cb9c2f2e`  
		Last Modified: Wed, 22 Oct 2025 20:17:38 GMT  
		Size: 1.0 MB (1045726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894e3c663b4cc1ec0c761a0ab4794a5d35210b323de22d97bda13c6458f95606`  
		Last Modified: Wed, 22 Oct 2025 20:17:39 GMT  
		Size: 17.2 KB (17206 bytes)  
		MIME: application/vnd.in-toto+json
