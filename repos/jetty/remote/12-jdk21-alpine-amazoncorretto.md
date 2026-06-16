## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:a3a344a3485ac2ce39b6ae2441e0c5e556f35d78baf33b584ca20aaf670879ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:052fa9b091288bb35471fcfec45e39c44fc8e202409f7a6b06e79295509360ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220726107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c4c3ac1f46974faf7e2695b07e44f64d43268161517e38bf3b7ce2b800c191`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:27 GMT
ARG version=21.0.11.10.1
# Tue, 16 Jun 2026 00:19:27 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:27 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:17:16 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 16 Jun 2026 01:17:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 16 Jun 2026 01:17:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 16 Jun 2026 01:17:16 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 16 Jun 2026 01:17:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:17:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 16 Jun 2026 01:17:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 16 Jun 2026 01:17:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 16 Jun 2026 01:17:16 GMT
WORKDIR /var/lib/jetty
# Tue, 16 Jun 2026 01:17:16 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 16 Jun 2026 01:17:16 GMT
USER jetty
# Tue, 16 Jun 2026 01:17:16 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Jun 2026 01:17:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:17:16 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989fc81d937729a00dafca55dbd23dc5a68a72a2a59d2f999819aa71fc5c941f`  
		Last Modified: Tue, 16 Jun 2026 00:19:47 GMT  
		Size: 161.8 MB (161837219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32cd6a42690a913b0c9df2f07cfdce754c3cff4dd74ebbcdd4aed54013e29a6`  
		Last Modified: Tue, 16 Jun 2026 01:17:27 GMT  
		Size: 55.0 MB (55040621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087868b4378947511038b8c9455ebb41f680335ca546c9a3c1bf53e7c1993326`  
		Last Modified: Tue, 16 Jun 2026 01:17:26 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:6269cb8471f147ea82f93ede3a17407f638ab896556ece92dc4c1349906aba14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1030100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876fbd40210d0b88adaba1feb50ff29a678c63c9d4852be2d2b1249583308d86`

```dockerfile
```

-	Layers:
	-	`sha256:5410e8b23ef4bbefb0015592707a014bc52c1ae3d51ccacddac2e80dae66bc86`  
		Last Modified: Tue, 16 Jun 2026 01:17:26 GMT  
		Size: 1.0 MB (1013025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0320f1d2b95833f0a86950a1e9172e15f0e8eddbd1768c8a1031a5cd83fd8abd`  
		Last Modified: Tue, 16 Jun 2026 01:17:25 GMT  
		Size: 17.1 KB (17075 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:87cfefcde036460c0024dba429d35fec8b7ffc22901185322ca17c3f6b1baa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218953602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc407046e5e17454e77c6eaf8f64c1dc8bf6c63eeea79a32239026146e067773`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:35 GMT
ARG version=21.0.11.10.1
# Tue, 16 Jun 2026 00:17:35 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:18:22 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 16 Jun 2026 01:18:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 16 Jun 2026 01:18:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 16 Jun 2026 01:18:22 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 16 Jun 2026 01:18:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:18:22 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 16 Jun 2026 01:18:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 16 Jun 2026 01:18:22 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 16 Jun 2026 01:18:22 GMT
WORKDIR /var/lib/jetty
# Tue, 16 Jun 2026 01:18:22 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 16 Jun 2026 01:18:22 GMT
USER jetty
# Tue, 16 Jun 2026 01:18:22 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Jun 2026 01:18:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:18:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77b0e734531ffce2dd53a41d8efbea96cb25eff325d8480cac6ef130b7bb81`  
		Last Modified: Tue, 16 Jun 2026 00:17:54 GMT  
		Size: 159.8 MB (159841745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f85d80d972fc74bce06cc9498a717c8e7fcc8462a1d4507fa03f183701ac838`  
		Last Modified: Tue, 16 Jun 2026 01:18:33 GMT  
		Size: 54.9 MB (54926944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b6a54aa5fb8d735b680477536a66ace6b09151aff423f7b05ecdb809a639d`  
		Last Modified: Tue, 16 Jun 2026 01:18:31 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:26710ec5e2daa3a5c2b6488fbb00dea94d4305060dba345c6152b5dee4e22346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1028950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb0f35f77fef0a8390809d7336a81f56d4216211d7d99e3604cf7f509da7898`

```dockerfile
```

-	Layers:
	-	`sha256:d4bcfaa3aeed30382b4de55692941bc40f9b322281c469d15f6a130983e2894f`  
		Last Modified: Tue, 16 Jun 2026 01:18:31 GMT  
		Size: 1.0 MB (1011782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4869b37e4e1f2d3698e44b981b5cccb441c49314488721ffbaf9e6fc9ac18d2a`  
		Last Modified: Tue, 16 Jun 2026 01:18:31 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json
