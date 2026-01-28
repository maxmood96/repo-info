## `jetty:11-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:aebe4a8ba80c019a69702aebf3b14548458eca456ad5f3616de8399b7311418e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:e1a18bbf186df3370a8b6705d75a269e176d58845b7c29cf70dbd50cf11353ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175990749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0b75bca87cfcfec640620a7e13459923dd7d2def1c6f35fd6bd53c3b378eae`
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
# Wed, 28 Jan 2026 04:17:49 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 28 Jan 2026 04:17:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:17:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:17:49 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:17:49 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:17:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 28 Jan 2026 04:17:49 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:17:49 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:17:49 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:17:49 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:17:49 GMT
USER jetty
# Wed, 28 Jan 2026 04:17:49 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:17:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:17:49 GMT
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
	-	`sha256:cf09f60ff094629e827ee932004afa2e86687339472f6c099d8f51f1b8822860`  
		Last Modified: Wed, 28 Jan 2026 04:17:58 GMT  
		Size: 23.8 MB (23759890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d422fc0053e39356b59a3b05e0b733493a0c26c4b11983a99f5528d2805bf86`  
		Last Modified: Wed, 28 Jan 2026 04:17:57 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:2e6abd121990bbfc2affac8c95847518c50ba43c2da5ca7b3b3d5df1df08a758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c414c7639e78112cd1595f9adbdd50df122d47c8c5329bf7e8933c833abefcc`

```dockerfile
```

-	Layers:
	-	`sha256:0131859b90d43598895c97b330e9da7de225cfc16578aca917692c1cec480d74`  
		Last Modified: Wed, 28 Jan 2026 04:17:57 GMT  
		Size: 823.8 KB (823761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e3f45fec7443c3903251c1980875a69d345cd41e33473655b678440b5bd12b`  
		Last Modified: Wed, 28 Jan 2026 04:17:57 GMT  
		Size: 17.1 KB (17075 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:f9cc7bf7a4c14802ab84d0b6ac969a000ec3f80751093d4a48908dcb27e8fbb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174572225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7679fa0a70d190bbb7656802a3c8a5098a498d1d507f905a933e7bdecf4597d`
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
# Wed, 28 Jan 2026 04:36:50 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 28 Jan 2026 04:36:50 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:36:50 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:36:50 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:36:50 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:36:50 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 28 Jan 2026 04:36:50 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:36:50 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:36:50 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:36:50 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:36:50 GMT
USER jetty
# Wed, 28 Jan 2026 04:36:50 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:36:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:36:50 GMT
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
	-	`sha256:3f7f71899c9a669960dd1651b6f8bcabf0961be8afdbaa206754fa6bbba9718f`  
		Last Modified: Wed, 28 Jan 2026 04:36:58 GMT  
		Size: 23.7 MB (23660477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bc062415dd13d4cd2ab57bd2483065f7e213962d43c18205926b2c109f90c`  
		Last Modified: Wed, 28 Jan 2026 04:36:58 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:aebec5cd4c39ebd8524cb984297032133c392d62de2f981899c2fd95497ff05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.7 KB (839686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cc7430daa757dd864551d8ec1c69685b3a9a138cf8762ce42f494033e9580b`

```dockerfile
```

-	Layers:
	-	`sha256:8960dd549836d605dacf53b304d77202bf3ce2387c5c3b94835bf781939a2a53`  
		Last Modified: Wed, 28 Jan 2026 04:36:58 GMT  
		Size: 822.5 KB (822518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efeaad3550aba2113e501e0fe1f506aa9c2183aaa10301460d9384ced45c60b4`  
		Last Modified: Wed, 28 Jan 2026 04:36:58 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json
