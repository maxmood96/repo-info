## `jetty:12-jdk25-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:8a2e50dd7fe99989b4ab84d605b9fca0b9866ce741c16dcea0a589d462c6d26b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk25-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:ce071262a77a985947efa6082019c8bed4772134099586724d07703e4c94dce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239930893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01990c9876423a13fb582d2e5bad0a8b5ae5702835ba406e2076be4b739d8fcd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:23 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:23 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:23 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:13:10 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 22 Apr 2026 22:13:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Apr 2026 22:13:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Apr 2026 22:13:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Apr 2026 22:13:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:13:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 22 Apr 2026 22:13:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 22 Apr 2026 22:13:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 22 Apr 2026 22:13:10 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Apr 2026 22:13:10 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 22 Apr 2026 22:13:10 GMT
USER jetty
# Wed, 22 Apr 2026 22:13:10 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 22 Apr 2026 22:13:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 22:13:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6130299703f5831bc35b5254b4eb5549c81fd91109769f9225c20dd65844ae64`  
		Last Modified: Wed, 22 Apr 2026 21:35:44 GMT  
		Size: 181.0 MB (180998980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92eb6103851c59052d610f05f26eb71cd7a2543d7b54a7e9d34c327c9309338b`  
		Last Modified: Wed, 22 Apr 2026 22:13:22 GMT  
		Size: 55.1 MB (55065848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591e9d85f8a1f29ee1cb37c43e7149fbe1617815e256d8062321baa176453765`  
		Last Modified: Wed, 22 Apr 2026 22:13:21 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b3e6e4fbac707f44821ec963c0a977d49dece670e30d057133bd6a3f0436f8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70b5a2fe072f986939d25a236d3ccd9ee1b27cc830bd178b496c4f251830e9f`

```dockerfile
```

-	Layers:
	-	`sha256:d2f77d2060a11fa2b200810f5b8126a75c67a53e93cfa79036f8b5ce32ecd6ee`  
		Last Modified: Wed, 22 Apr 2026 22:13:21 GMT  
		Size: 1.1 MB (1053558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57ace09b4518c0365fdbc87a3cd82ea6e5e589cf4c31094b5295c271de5281f`  
		Last Modified: Wed, 22 Apr 2026 22:13:21 GMT  
		Size: 17.1 KB (17071 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk25-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:bc5c7db1837a602aa71ecb47ca01eab4140db9d2444fc8ec35c5e3ab4cdb1a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237787652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c379276ac30ba4400c6fefd20de63130f2705cd8bdbce603e52914714c4382ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:17 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:17 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:13:01 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 22 Apr 2026 22:13:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Apr 2026 22:13:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Apr 2026 22:13:01 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Apr 2026 22:13:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:13:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 22 Apr 2026 22:13:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 22 Apr 2026 22:13:01 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 22 Apr 2026 22:13:01 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Apr 2026 22:13:01 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 22 Apr 2026 22:13:01 GMT
USER jetty
# Wed, 22 Apr 2026 22:13:01 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 22 Apr 2026 22:13:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 22:13:01 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d236e04af56142e3286d8350a8586b6e1a108498823e2f4b6b22a514d970c21`  
		Last Modified: Wed, 22 Apr 2026 21:35:40 GMT  
		Size: 178.6 MB (178621799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539f6801bb8635a90cdf90592f992d52100e90167bc5259e19b82c25b2dfacb1`  
		Last Modified: Wed, 22 Apr 2026 22:13:13 GMT  
		Size: 55.0 MB (54964106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fd9ce57eacd77fe3aca325d50d1cf4b35cf395dc6c8cb09ea0851f51e8eca9`  
		Last Modified: Wed, 22 Apr 2026 22:13:12 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ab83f62f111b3237540041b2600d17cddc36b02d6b3768f6cebe06c5e64d3a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1069475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2d532c184d7c539777d8c3364d00568de7bfedfb1353b593a7f9e8aafd9bd3`

```dockerfile
```

-	Layers:
	-	`sha256:f76d9ca9b9cb028746146c583dc1f9be1b9cc45f6342d8e9ff0056999b9d6d88`  
		Last Modified: Wed, 22 Apr 2026 22:13:12 GMT  
		Size: 1.1 MB (1052312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3a7710b910be71bea2725ba0b53d537f4e16dbaf2eb3e16b171b5386a678eb`  
		Last Modified: Wed, 22 Apr 2026 22:13:12 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json
