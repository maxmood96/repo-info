## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:dbda1e20a6555d6890f209ee220d07fadd7c77b89ff007ba437006a3d779776a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:6bec3d0186b990642e8ede7738f6a22e2017e592b7a2520d87acaa035c7f70bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 MB (220308174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867885eb41e750a73e145b659657869b796609745ae07dd029ea4852a93a13d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 00:19:17 GMT
ARG version=21.0.9.10.1
# Thu, 09 Oct 2025 00:19:17 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 09 Oct 2025 00:19:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_VERSION=12.1.2
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.2/jetty-home-12.1.2.tar.gz
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 09 Oct 2025 00:19:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
USER jetty
# Thu, 09 Oct 2025 00:19:17 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Oct 2025 00:19:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Oct 2025 00:19:17 GMT
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
	-	`sha256:4df741ae75a25f63b36432fed81267b4ff8fae6e778ddf645a9a435f4f0447c3`  
		Last Modified: Wed, 22 Oct 2025 02:40:03 GMT  
		Size: 54.9 MB (54926302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072d5f46d8c4285a23b3caf39c2f9968235ea55bc2814024f9360db974d6beac`  
		Last Modified: Wed, 22 Oct 2025 02:39:57 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:72b76e7fdbe1609846796a1141499c5b2aa820214d1b8ede996514a51dc413d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9ceefcc9f88025da9e17f58fb421db5d760d3753f13a4e1b5457b5093e1dcc`

```dockerfile
```

-	Layers:
	-	`sha256:1819a38f74a91dbd578bd0833d4ba722a96a7aa4cdf37a1929053a595d52aba3`  
		Last Modified: Wed, 22 Oct 2025 05:18:30 GMT  
		Size: 1.0 MB (1046319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6459df8f2ebc75c6f507c2efcdf56b3f1ad2ba5cf249dbbba4ba3d975cd571d8`  
		Last Modified: Wed, 22 Oct 2025 05:18:31 GMT  
		Size: 17.1 KB (17113 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:4dc0a65399fecce177c7884c55a3ad918f8d93296ed945d1b1eabf3c3838a72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218566308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ca1b2f667fb037d7d78d870343c372fa11ad9d22bff4ab67f4f7d8882c8aa9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 00:19:17 GMT
ARG version=21.0.9.10.1
# Thu, 09 Oct 2025 00:19:17 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 09 Oct 2025 00:19:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_VERSION=12.1.2
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.2/jetty-home-12.1.2.tar.gz
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 09 Oct 2025 00:19:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
USER jetty
# Thu, 09 Oct 2025 00:19:17 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Oct 2025 00:19:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Oct 2025 00:19:17 GMT
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
	-	`sha256:e3f88c5cfdd21af16410f1b2d51c07b7814f71b74d414d73760a1f3a4be1509c`  
		Last Modified: Tue, 21 Oct 2025 22:14:02 GMT  
		Size: 54.8 MB (54831247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55221c26c372c9c6deabfd2adfc8feff3e1ce1270b98effbead0c8ded41caa7c`  
		Last Modified: Tue, 21 Oct 2025 22:13:53 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:727bc20289453cd43d7aae642f1edee8a6c27b534d93d0f9181192b7a9396746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391ed9db39a3c4a8884e63fb904b9e6663ca6067475f1aa0f730fdd761ab44b9`

```dockerfile
```

-	Layers:
	-	`sha256:85cdb214ba16826cb517c26286773f4e242d2ed7713a480cc44afc1bf07f5fdf`  
		Last Modified: Tue, 21 Oct 2025 23:18:17 GMT  
		Size: 1.0 MB (1045726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6331232560cf9de1e130cde95c17994890a62bf2379f06ee84ade049a0f588d4`  
		Last Modified: Tue, 21 Oct 2025 23:18:17 GMT  
		Size: 17.2 KB (17206 bytes)  
		MIME: application/vnd.in-toto+json
