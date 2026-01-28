## `jetty:10-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:252e26e609846777ce2890953236d7196d975c763384cfc28a54e44f88a91be0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:958fc9568ccf8d152d4ae57c525dfcf3ae26219c1681c0d0d646a40d99a925a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172546900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e960157daae2182d49c948712bf5edae89d01898f9a12547bd8f9c661550e126`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:48:03 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:48:03 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:48:03 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:48:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:48:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:18:07 GMT
ENV JETTY_VERSION=10.0.26
# Wed, 28 Jan 2026 04:18:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:18:07 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:18:07 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:18:07 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:18:07 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Wed, 28 Jan 2026 04:18:07 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:18:07 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:18:07 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:18:07 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:18:07 GMT
USER jetty
# Wed, 28 Jan 2026 04:18:07 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:18:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:18:07 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ed859fda71dc33d0955acbbb721804c828661acbb1012ae01e3ff3c4843fff`  
		Last Modified: Wed, 28 Jan 2026 02:48:20 GMT  
		Size: 148.4 MB (148367161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae943a8cd86184d4d9625838a7acc5df7681b615f95b21e0efeb113e6044e62`  
		Last Modified: Wed, 28 Jan 2026 04:18:17 GMT  
		Size: 20.3 MB (20316041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c0b376c45921d60a1478567297eb4196d35f27a5b727eca877ad17674e5aa`  
		Last Modified: Wed, 28 Jan 2026 04:18:09 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:818967a08254eaf0342c87625479eaed9c201799c3e5a37a35f5c51d64954a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b288e1b32097630256ea88f694e3753df8ec233b82817ec1065cdbb1537c71`

```dockerfile
```

-	Layers:
	-	`sha256:facb8e207f19475812b19d7fee78f03ef6a00c2ccf8035480bad01e108fd151b`  
		Last Modified: Wed, 28 Jan 2026 04:18:16 GMT  
		Size: 823.7 KB (823711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2efda31b0ce27757b1904639e2c6c96af6778931f21e18c2e33737cb03dd992`  
		Last Modified: Wed, 28 Jan 2026 04:18:16 GMT  
		Size: 17.1 KB (17076 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:22a4349587f048ce53b1bf9016dae0e2d3ee7a9d16e7d1de9316a92550d22cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171128014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae6f67c4879ed2f265cfd88d64e296307aa0f09d9846b8d50e7b8e3166737cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:18 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:49:18 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:49:18 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:49:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:49:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:37:04 GMT
ENV JETTY_VERSION=10.0.26
# Wed, 28 Jan 2026 04:37:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:37:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:37:04 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:37:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:37:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Wed, 28 Jan 2026 04:37:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:37:04 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:37:04 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:37:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:37:04 GMT
USER jetty
# Wed, 28 Jan 2026 04:37:04 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:37:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:37:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd0167a09da280b97a0fb6dce8bd4a2fd4b5ad1e8a8869f0be19e804f371840`  
		Last Modified: Wed, 28 Jan 2026 02:49:36 GMT  
		Size: 146.7 MB (146712780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac78f7b6675f50044f9c0b420a6694af82327a90ef6692456261a2a3e3062266`  
		Last Modified: Wed, 28 Jan 2026 04:37:13 GMT  
		Size: 20.2 MB (20216267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617511f2de143991f7feffb564b4f0a3964754f5fac6a62e6dbfdef60eb745c`  
		Last Modified: Wed, 28 Jan 2026 04:37:12 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:dd81845c47250b21d58fe6bbcbcba723ab2015817a591f0488f877a7b742d325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.6 KB (839636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273ccafb0079f0e1f0e2c0252afe5ed3caa64c8e8f89c565b16814e96914eb78`

```dockerfile
```

-	Layers:
	-	`sha256:50a87f733f2ac2ab18c0d634b874fe8350709c667f5c89d027e8e4bc3b8807ba`  
		Last Modified: Wed, 28 Jan 2026 04:37:12 GMT  
		Size: 822.5 KB (822468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c06d20519af35310c95688e5faa5382663980e0c289e0486e9f2e3d082a2d5c`  
		Last Modified: Wed, 28 Jan 2026 04:37:12 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json
