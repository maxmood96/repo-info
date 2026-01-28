## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:7ec6c2183d956300013550cc31c6f263c773b9dedffe66db20b7ca6b27d2c5bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:992f39346cb54409d9a22c874fe03e78210f7a42af28754852d06f5e93f85b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220695596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0f937401f99a13728e2c1d9d03eea767e4e0754ae4c92ae0a5f82aa1b6566c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:15 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:15 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:19:11 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 21 Jan 2026 19:19:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:19:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:19:11 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:19:11 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:19:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 21 Jan 2026 19:19:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:19:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:19:11 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:19:11 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:19:11 GMT
USER jetty
# Wed, 21 Jan 2026 19:19:11 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:19:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3b5bdb09ad91d86c575799ac71f0f8e4cf37a35be2c5430890f6cad8a53919`  
		Last Modified: Wed, 21 Jan 2026 19:01:34 GMT  
		Size: 161.6 MB (161590231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64082f26cef97ab3b6a7de5112087c2f23bbdd1fb08c30a27553763d75fb50b`  
		Last Modified: Wed, 21 Jan 2026 19:19:24 GMT  
		Size: 55.2 MB (55243384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b272728747408d54f0689a0a91e5ff55099c5bbc8e4c462d4509ad5e7fdc554b`  
		Last Modified: Wed, 21 Jan 2026 19:19:22 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:84a80ee1b714fc67723d6b5ab9e295bf59820cfcd4995563428aff23d2d8e92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6785e388761fd737166d0937557ec56b12a1979067eee924da1abe675f7f2a4b`

```dockerfile
```

-	Layers:
	-	`sha256:8869a9259658ac21f7f06af8b7cbcce6d3600b2c2331df3733a4675af1fbae51`  
		Last Modified: Wed, 21 Jan 2026 19:19:22 GMT  
		Size: 1.0 MB (1046634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f87fb3f3db4a46fb9a2bd822ed0df257013ff045fbb8446b8c96346454a3d9`  
		Last Modified: Wed, 21 Jan 2026 19:19:22 GMT  
		Size: 17.1 KB (17071 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:90046e8aa8c33853f32015c27a374832edcb16561ec474154b7f5793e0365762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218959538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22c4cbfd38e050d38a37bc23636bdce93d67442a03e98a651a3b5498a8abe0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:51:47 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:51:47 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:51:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:51:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:51:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:36:10 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 28 Jan 2026 04:36:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:36:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:36:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:36:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:36:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 28 Jan 2026 04:36:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:36:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:36:10 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:36:10 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:36:10 GMT
USER jetty
# Wed, 28 Jan 2026 04:36:10 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:36:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:36:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b075c73c3fb61a2595fbd83c3d77b387659de25ba9b2d1de05f9d24ee5f70`  
		Last Modified: Wed, 28 Jan 2026 02:52:06 GMT  
		Size: 159.6 MB (159615593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5afb2b7d95a74a99a192641de34f25b94f4bb46fd25755a4565c6e21e6fb22`  
		Last Modified: Wed, 28 Jan 2026 04:36:21 GMT  
		Size: 55.1 MB (55144980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d78395b8fff71bc88871048b2168e1c34445a5432541113f34ea7ee0192678`  
		Last Modified: Wed, 28 Jan 2026 04:36:20 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f8e001acb73716837acae08eb9d172c77d867fe72732b912d6bd1fc18d179f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb318da062bda9cf72b7318add01d10fd2fe5095a0a8b3328e20dacbf94ade34`

```dockerfile
```

-	Layers:
	-	`sha256:36a330d466599f6af16c49ce314611ef5795fa473e44aeec08ce3df16d50f0e5`  
		Last Modified: Wed, 28 Jan 2026 04:36:20 GMT  
		Size: 1.0 MB (1045391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39badcf06b3b61a0335c92922634744961d9c849b82d93fc18221d776cea8ddf`  
		Last Modified: Wed, 28 Jan 2026 04:36:20 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json
