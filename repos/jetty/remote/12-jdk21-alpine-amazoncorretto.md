## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:32c38cc324d52f6a14fecea479df0b6c5d8d2e243d652e520943ef4e67de85fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:b93d77853cd7ba8209c14c0377012dadb2cf690f44a06f21f2c8908507f6bc5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218093376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797ade8a8fbb8cc21e28fcbd4add03bbd89c50a8daa68448530bf8d35e2c34cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_VERSION=12.1.1
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.1/jetty-home-12.1.1.tar.gz
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Sep 2025 00:35:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
USER jetty
# Tue, 09 Sep 2025 00:35:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Sep 2025 00:35:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Sep 2025 00:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b083f149c2d267ca3303423ef9bf313bd8ed46afb1e9070b278f0f1cc4924e65`  
		Last Modified: Fri, 18 Jul 2025 20:07:40 GMT  
		Size: 159.4 MB (159384044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc62b749d8ab5644638ba4cb53a291ac51baec23c798691017465031f578be92`  
		Last Modified: Wed, 10 Sep 2025 16:27:46 GMT  
		Size: 54.9 MB (54907765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a72d6480e8ce4f50bf7514c60a6db4a74282025e20ff923286757279d2861bd`  
		Last Modified: Wed, 10 Sep 2025 16:27:34 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:51ab06f9b840b066e13830a4f20a619e39b5f1c36caa6dec2efe0c0aac14cad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 KB (865054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e89a498d854cae183c421dc2c89266bc61625bc07390785a1433a4368243a9`

```dockerfile
```

-	Layers:
	-	`sha256:e32c267b1cc465fe13ecc03581facf53a5f9e32968bd349376c343675c34e753`  
		Last Modified: Wed, 10 Sep 2025 17:17:41 GMT  
		Size: 847.9 KB (847940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6fe52428c0a37a2c6d721dbcde78a90bc60f2fff277d3789879e88f3a0502`  
		Last Modified: Wed, 10 Sep 2025 17:17:42 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:11ee296f38fa58c1f6bfbc3875b42cc166fed18472057811bec94795866dfe2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216286164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f49b238e9fe893a1295e883f65583692c505660740bbc665a5ec660e6b4444`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_VERSION=12.1.1
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.1/jetty-home-12.1.1.tar.gz
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Sep 2025 00:35:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
USER jetty
# Tue, 09 Sep 2025 00:35:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Sep 2025 00:35:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Sep 2025 00:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d02d07fda222ee822c634825bb45fa7a804b9bd3c8234251bbb38d689f3ade`  
		Last Modified: Fri, 18 Jul 2025 20:16:42 GMT  
		Size: 157.3 MB (157341766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d3823f2120d7a72a3fa5b79cba19dca5db5632a0549c5b8c30ffeacdd4a43a`  
		Last Modified: Wed, 10 Sep 2025 16:29:41 GMT  
		Size: 54.8 MB (54811771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a98e0b31fd70f7e53fb85faec794e2a7edf073dbdfc57305b2f22bfea02f23`  
		Last Modified: Wed, 10 Sep 2025 16:29:34 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:bd5a17809856388c09aff8fe292134806d37bcaaf57a2f759086af97374bca29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.6 KB (864553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf0fd47d0d8ce473781037553d94352cfbeabfe80482461156f4d2eb086c424`

```dockerfile
```

-	Layers:
	-	`sha256:c04b8775930ede06edcb00ea9646fe3818c99312678aead32c17107a2ed7e3fa`  
		Last Modified: Wed, 10 Sep 2025 17:17:46 GMT  
		Size: 847.3 KB (847347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab59404351d38cef130741bc6c682196f597b9bef6e153dbd5f7e56ac529f23`  
		Last Modified: Wed, 10 Sep 2025 17:17:46 GMT  
		Size: 17.2 KB (17206 bytes)  
		MIME: application/vnd.in-toto+json
