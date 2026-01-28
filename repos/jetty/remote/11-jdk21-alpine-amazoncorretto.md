## `jetty:11-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:ad91002585736d0513d30f8ddd4ab7f4047ded73e378554efd19ae8a11e5caf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:cc365a4bd2cfe0722a307334887a17505c4343187b2026aca0ed21ae370187b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189214119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb253dd40ef11e20a89c5ac18ed730ef4dc0e57c303219e92a828f9009615ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:24 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:50:24 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:50:24 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:50:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:17:41 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 28 Jan 2026 04:17:41 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:17:41 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:17:41 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:17:41 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:17:41 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 28 Jan 2026 04:17:41 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:17:41 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:17:41 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:17:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:17:42 GMT
USER jetty
# Wed, 28 Jan 2026 04:17:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:17:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:17:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0476ba18ce4a7d863df3375a1843d00caa67c25f77311a8828c2f340ca01d1fc`  
		Last Modified: Wed, 28 Jan 2026 02:50:43 GMT  
		Size: 161.6 MB (161590292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8362b13654470d876a808a4e80c9baac74446157655d39fe991db08c5eb79fdc`  
		Last Modified: Wed, 28 Jan 2026 04:17:52 GMT  
		Size: 23.8 MB (23760130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6016f6281f6bf3a9c323a1e32f8ab7ee2ea58898cf314f7a6901b0869998461`  
		Last Modified: Wed, 28 Jan 2026 04:17:50 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:97f38ded444e3ea3865b91d840ec58fcf65481a3829aa4720671fa4738ecfb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.7 KB (840740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc1628d2f29513daf2614ec33eee7aff44d048ed481319bf126f23968968b53`

```dockerfile
```

-	Layers:
	-	`sha256:a5bd1379bdf6d306e2f49eec8ea45a840a4da9939793252c500227ef5f7af835`  
		Last Modified: Wed, 28 Jan 2026 04:17:50 GMT  
		Size: 823.7 KB (823664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b6c41631ac78079767168ab41eb76946d887f69b56e707b64684d356632231`  
		Last Modified: Wed, 28 Jan 2026 04:17:50 GMT  
		Size: 17.1 KB (17076 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:9b3870d0bc0fe04b80cc50d57f1f214268571ef2ae0bf580ee99048469f3df0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187475001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7664efc36361c3d65325e609c2ac6f098fb8ff2f16f13d204545bdaa8adf9807`
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
# Wed, 28 Jan 2026 04:36:38 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 28 Jan 2026 04:36:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:36:38 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:36:38 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:36:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:36:38 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 28 Jan 2026 04:36:38 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:36:38 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:36:38 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:36:38 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:36:38 GMT
USER jetty
# Wed, 28 Jan 2026 04:36:38 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:36:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:36:38 GMT
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
	-	`sha256:c14d6cf1c66d38920639a5fd84689935a947382d9d32ab227a2e6d977d60e168`  
		Last Modified: Wed, 28 Jan 2026 04:36:47 GMT  
		Size: 23.7 MB (23660441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4272b0fcb97090bf940cd84d58a1dfd6c30f877775653a0bcc36966a908be1b9`  
		Last Modified: Wed, 28 Jan 2026 04:36:46 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9938789b6857b1371547a81bb8a9822d974d4fd1bb44b0ac29ead8e9bac229ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.6 KB (839589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521f11c4bef7086587a23335d76785437bc3307fe0d077b209cdc6b490074ef1`

```dockerfile
```

-	Layers:
	-	`sha256:ca06328be521bb7d0a8af272852549a7ea497977cca61c15442fb384817cc6f1`  
		Last Modified: Wed, 28 Jan 2026 04:36:46 GMT  
		Size: 822.4 KB (822421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c83b320ca3eca4aef46d45d65b5bbae87d7fd7d42dd50327d27021d6270684`  
		Last Modified: Wed, 28 Jan 2026 04:36:46 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json
