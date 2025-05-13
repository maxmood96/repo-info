## `jetty:12-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:0c3ad13afc6c0e99cc9d5001cdad4b620ec834edf012a00fe9a38e6419793284
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a868aefb69033ee89af0abab47bf16d9955e0ebde4ca6c913f958e332a1d02b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192828146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ca16b80d7c1e70a0ac07ab84cc2ea021c769023ae170218df72f45d7708b99`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_VERSION=12.0.20
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.20/jetty-home-12.0.20.tar.gz
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 13 May 2025 01:11:22 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 13 May 2025 01:11:22 GMT
WORKDIR /var/lib/jetty
# Tue, 13 May 2025 01:11:22 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 13 May 2025 01:11:22 GMT
USER jetty
# Tue, 13 May 2025 01:11:22 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 01:11:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 May 2025 01:11:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5df5939bdcf113ce439bdcecfe24681c539b1c385300c7ef0aa8ff1d356a6f8`  
		Last Modified: Tue, 15 Apr 2025 23:55:45 GMT  
		Size: 145.8 MB (145751782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecd0b5317a9c2405fa41b2bfb8b8846cd55e9a495433472e7d947e7b26ba944`  
		Last Modified: Tue, 13 May 2025 18:25:20 GMT  
		Size: 43.4 MB (43432425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9a8869acf09fb86bddc46ecb2a3011977a19a4a0985174e389be719cbe43ea`  
		Last Modified: Tue, 13 May 2025 18:25:19 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:66ec21bc2777fff04d272986014a0998d7456c154b4f79f4e4d5a640653a6f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.7 KB (749695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e657edb621893e875c5dc41b4df2a36011c1e35aa980f3f06e82cf7245dfef`

```dockerfile
```

-	Layers:
	-	`sha256:21b0694852da61d7a9e9d77865c6973639f958241e67bf55b7c53c8a2dc8bbef`  
		Last Modified: Tue, 13 May 2025 18:25:19 GMT  
		Size: 732.6 KB (732576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665d40708f991c74dc165305e6e69619fc99c50d1b4cba8edf6f05b3175d94ac`  
		Last Modified: Tue, 13 May 2025 18:25:19 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:673e033deea2b3273356c4e465110fab44bab9124092a5f518b3cdf70410a5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191423852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d07f4c3439eb37f9e660598a109627f4ebf59ea03fb440dafac602c2549455`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_VERSION=12.0.20
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.20/jetty-home-12.0.20.tar.gz
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 13 May 2025 01:11:22 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 13 May 2025 01:11:22 GMT
WORKDIR /var/lib/jetty
# Tue, 13 May 2025 01:11:22 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 13 May 2025 01:11:22 GMT
USER jetty
# Tue, 13 May 2025 01:11:22 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 01:11:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 May 2025 01:11:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214ed60a36622070a258d17b66c8af5d000fe6f8f37ad1321be41f65e590e9b1`  
		Last Modified: Wed, 16 Apr 2025 00:15:04 GMT  
		Size: 144.1 MB (144095821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b5cbc789765e9a5ba6ef340d4f0196a500be48f9c0b6f51cea4a3c8ea621ba`  
		Last Modified: Tue, 13 May 2025 18:32:00 GMT  
		Size: 43.3 MB (43333311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fc4fecff858041a102746de1525ee0848aac1514e49856fef8f1732216e8ab`  
		Last Modified: Tue, 13 May 2025 18:31:59 GMT  
		Size: 1.7 KB (1659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1908ce11ee343e1ad37c4c8e00ca3ee78c864ce3e05d39f43aae67d51647c1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.2 KB (749194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb157dfbf60c62fd1aade6515302afb9c14595d32f2adadfe285a2e054e3112c`

```dockerfile
```

-	Layers:
	-	`sha256:2dab0a6ad901b130d3c968d97d78368970f01a097127bd72df2f48f5434477ec`  
		Last Modified: Tue, 13 May 2025 18:31:59 GMT  
		Size: 732.0 KB (731983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c8824ef241846a95d73466c900a74ac9115843cf16c67e2c22b3da2c90e076f`  
		Last Modified: Tue, 13 May 2025 18:31:59 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json
