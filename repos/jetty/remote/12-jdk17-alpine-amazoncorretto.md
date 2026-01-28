## `jetty:12-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:594b0037ce8ab5afa8be3b2683beba0494e4fe4a682542e3e94ee96eb175804c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:61f5668d40dc9dbbd63e3c5d20e5532042c254bf6746fe412237f5dbde44b73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207473948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0815290f1ef554876cff19100ea2f0a7ec1fd16fe8c33f3ffd5b7faddeaca0e6`
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
# Wed, 28 Jan 2026 04:17:13 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 28 Jan 2026 04:17:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:17:13 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:17:13 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:17:13 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:17:13 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 28 Jan 2026 04:17:13 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:17:13 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:17:13 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:17:13 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:17:13 GMT
USER jetty
# Wed, 28 Jan 2026 04:17:13 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:17:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:17:13 GMT
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
	-	`sha256:ced14193cd06e4d332b0afb0a70290e3746041192946de35fda4f98633343902`  
		Last Modified: Wed, 28 Jan 2026 04:17:24 GMT  
		Size: 55.2 MB (55243090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c772a9a42ae8fb4e77accf12ef69afe161af64684e63ba247b592d83413c35f8`  
		Last Modified: Wed, 28 Jan 2026 04:17:22 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:247d99f01ed02c8fb84fdd7b816bb590d0148d76c3f6e94815b616ea7f081fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856d84e421e22e9a9fa4e101a9eeb568090976bc13c3ae07d6662bc2a0e819a2`

```dockerfile
```

-	Layers:
	-	`sha256:70d5582dcba9cb0eb8153c96fd0e23e379880cf1d37b5fb7875aa760fc81597d`  
		Last Modified: Wed, 28 Jan 2026 04:17:22 GMT  
		Size: 1.0 MB (1046731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90fe02984a464020a4d578b454c74af52f46fd04eea221003a8cf169e4188f6`  
		Last Modified: Wed, 28 Jan 2026 04:17:22 GMT  
		Size: 17.1 KB (17071 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5ba274b51d5a4d18eaba17b4a97d50675e8d002453d3bf1bc0ef1ae4395cfbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206056742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2322789fce3f63d1e960f1b6d7bb5736c63edbf76b62d12da31cdd4afe302ec`
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
# Wed, 28 Jan 2026 04:36:18 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 28 Jan 2026 04:36:18 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:36:18 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:36:18 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:36:18 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:36:18 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 28 Jan 2026 04:36:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:36:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:36:19 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:36:19 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:36:19 GMT
USER jetty
# Wed, 28 Jan 2026 04:36:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:36:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:36:19 GMT
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
	-	`sha256:7d1bbd44252459600aee5bef51203db3fd9fb74079fbb369061380084230a160`  
		Last Modified: Wed, 28 Jan 2026 04:36:30 GMT  
		Size: 55.1 MB (55144994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ce74a3e69ab8020ebf4a96bc9e202a25deeeb50be96e664c27433bb161d895`  
		Last Modified: Wed, 28 Jan 2026 04:36:28 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5215fc9f57ee1dbfe0ab2ce3a460fbdb40a86bc6806147b702b6cb472127bfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccf1128865ccdd8b10440de93605a12d17d74dc1e127c8beee00d4c3ba80e42`

```dockerfile
```

-	Layers:
	-	`sha256:e6a408e2e383b57a50d7533f5a59880c99b020a24cea1acfc3ea603a8b136c1f`  
		Last Modified: Wed, 28 Jan 2026 04:36:28 GMT  
		Size: 1.0 MB (1045488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6496078c3191ec35acea6763edda27fd7a3a6e6a76047ba7aeb56ea46b530e01`  
		Last Modified: Wed, 28 Jan 2026 04:36:28 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json
