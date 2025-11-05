## `jetty:9-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:fb4892b004caafee1fa8900c3d7b6d3d7c3e8f54af5ebc7c58b564c9cd76294e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d132b2ff4d246b8edf9680b772863efd5cae61ba7d0702c43d809aa5353f9a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184570821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccc2d2eb298b8d9974e84927621a5057bf4dd7cc05cf723936d08e7fce692ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Aug 2025 04:54:08 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 04:54:08 GMT
ARG version=21.0.9.10.1
# Fri, 15 Aug 2025 04:54:08 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
ENV LANG=C.UTF-8
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 15 Aug 2025 04:54:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Aug 2025 04:54:08 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
USER jetty
# Fri, 15 Aug 2025 04:54:08 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Aug 2025 04:54:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Aug 2025 04:54:08 GMT
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
	-	`sha256:0460eafc2f0578028b60db83b27dd36bcdc60b6eae52af012fbf585347eceec7`  
		Last Modified: Wed, 22 Oct 2025 02:39:16 GMT  
		Size: 19.2 MB (19188949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3781be7cd1247d123ce10e2a0bd290f6d3c1fc8828b4f05806b11fa5eee6c266`  
		Last Modified: Wed, 22 Oct 2025 02:39:16 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:baf5286e1497a55a57da61b2743bc86831414fa3433304ea17857f51fd720b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.2 KB (826185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1a8ff9790c1e89076d9e40021ecdd3c5a93f27d8e7759ecbfc3ab29fb73cf9`

```dockerfile
```

-	Layers:
	-	`sha256:88571b803c248f94125104ef0fae8f4e872edf76fe3fc109c0ce38cd2b2aa3d9`  
		Last Modified: Wed, 22 Oct 2025 05:20:44 GMT  
		Size: 809.0 KB (809036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea3b51f4559d9e317c6da8d95870de94b31347027b841857e88a4ea2df9b0627`  
		Last Modified: Wed, 22 Oct 2025 05:20:45 GMT  
		Size: 17.1 KB (17149 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:8754d1b38ba2c776223e5c654a261f6f0bac69d087f52da0a36fad256b3a9c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182822839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4de4bf1733042115cde2eab5a7402f35bacde4b5ca218aaa0197660d547a84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:21 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:16:21 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 04 Nov 2025 23:25:45 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 04 Nov 2025 23:25:45 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 04 Nov 2025 23:25:45 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 04 Nov 2025 23:25:45 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 04 Nov 2025 23:25:45 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 04 Nov 2025 23:25:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 04 Nov 2025 23:25:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 04 Nov 2025 23:25:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 04 Nov 2025 23:25:46 GMT
WORKDIR /var/lib/jetty
# Tue, 04 Nov 2025 23:25:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 04 Nov 2025 23:25:46 GMT
USER jetty
# Tue, 04 Nov 2025 23:25:46 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 04 Nov 2025 23:25:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 23:25:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fd450f0185222facf50c3585803b24553a293cbfa900eb12641a7831d0da01`  
		Last Modified: Tue, 04 Nov 2025 23:25:34 GMT  
		Size: 159.6 MB (159588499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9913e6cea8b20059a4036705cdf33d1709f0520ab0a616dcb559e5ac3784cd`  
		Last Modified: Tue, 04 Nov 2025 23:26:00 GMT  
		Size: 19.1 MB (19094395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef94604eeacdcba9cd53e439e614ac71bd83737d2dbb505bdee8f145b85216bd`  
		Last Modified: Tue, 04 Nov 2025 23:25:58 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:10ef18c924aee11e130e3289ee4de94e90f77f6b704c686c56680a1a3095b59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.6 KB (825641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e8a6a608bf4feb91856b151df5ab2dcb2b826d271fb89627880a3693c471c9`

```dockerfile
```

-	Layers:
	-	`sha256:2477000bd1a740ba23fe268f491dc2a6c71568a63a0effa0850e1fe34272e1d0`  
		Last Modified: Wed, 05 Nov 2025 00:19:38 GMT  
		Size: 808.4 KB (808443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e145c91c8d67dc5a7ceac0e5f024c37b9c575ed06920728ff46a6f248a7c29`  
		Last Modified: Wed, 05 Nov 2025 00:19:39 GMT  
		Size: 17.2 KB (17198 bytes)  
		MIME: application/vnd.in-toto+json
