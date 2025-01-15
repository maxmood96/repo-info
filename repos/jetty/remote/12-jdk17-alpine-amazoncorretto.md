## `jetty:12-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:4195c466721b7f93e95b1553233ab516853ca2c47eb17768a21a5e674852f865
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:ab8ec296f657a8168123c06fb2015442db7856d980ee6a9db8178360cd951b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192783691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d2409ffb3ab48d75e6e7692a9f37c05794976fbf0a8f251ce6dc5c63c41f06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_VERSION=12.0.16
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.16/jetty-home-12.0.16.tar.gz
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 02 Jan 2025 02:56:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
WORKDIR /var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
USER jetty
# Thu, 02 Jan 2025 02:56:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 02 Jan 2025 02:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Jan 2025 02:56:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002f4b0a8700cfbf8303a06eadee575ca2c5115eda81e446e7e0f364c142303f`  
		Last Modified: Wed, 08 Jan 2025 18:13:27 GMT  
		Size: 145.6 MB (145649375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96807603331ac1456cfc8f47fa85f8cacd7ee8c9d978abf9f18bf8b0b381215c`  
		Last Modified: Wed, 08 Jan 2025 18:25:30 GMT  
		Size: 43.5 MB (43506391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e62fe8af6153a5d43660fe255296b2652168c404242fbd358c27cc99785e68`  
		Last Modified: Wed, 08 Jan 2025 18:25:29 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e257b2cf01cc545082b1fd55115a7b4520b9c46ae4cc53887b1c10a14f525d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.4 KB (841426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68522fe3c09b66992f7ea8c36140e2dd3c02a11cd05f0b5c3036f5f3c64010d6`

```dockerfile
```

-	Layers:
	-	`sha256:e69bd3680b0e6937f0219655bc15334bceb4aebd304a72ac5cb884b8cc22a14a`  
		Last Modified: Wed, 08 Jan 2025 18:25:29 GMT  
		Size: 824.3 KB (824307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f71e758288ec077f0c997921c8c3f5859d6b228b4ae3757c11a3d341c031cb`  
		Last Modified: Wed, 08 Jan 2025 18:25:29 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:b1aab08c5626c217fb8182b0695d205b7188eff3836d28a3bf058d8ccbfef427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191587043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f716a5df14398019048bee5777247047edcd6788abca1c09649cb47bc2b57b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_VERSION=12.0.16
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.16/jetty-home-12.0.16.tar.gz
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 02 Jan 2025 02:56:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
WORKDIR /var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
USER jetty
# Thu, 02 Jan 2025 02:56:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 02 Jan 2025 02:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Jan 2025 02:56:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29465d18296a94c04941e2979617086241bf2a9e47f8e09e5e32d73bc0d7587`  
		Last Modified: Wed, 08 Jan 2025 22:19:51 GMT  
		Size: 143.9 MB (143934718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f020cedbd1df5bb6c0c805f7568b291c63acb3cd9d98ef5c471a24e2c6bd279`  
		Last Modified: Thu, 09 Jan 2025 07:07:55 GMT  
		Size: 43.6 MB (43559890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d1c9f571d40072eadb6ea027f522243934e5f499c2378f617f400d78c47e`  
		Last Modified: Thu, 09 Jan 2025 07:07:53 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:7d3a96113e3356dae6528b62c14d6588da779d84b97e45e3b93bac15e3c980df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12e9a8eeb0161c3487f462bad4a013793bcc09eb2fae9b961ed3d90ff610051`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e1b8c6c5f198368000b1a4ea1f6e8b52caf61b1747301ad739aa854f4334`  
		Last Modified: Thu, 09 Jan 2025 07:07:54 GMT  
		Size: 823.7 KB (823714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab1a604d3823d641a9f83e38c0112169c1203e4e2db1ecf41b9ee1e5ac923fa`  
		Last Modified: Thu, 09 Jan 2025 07:07:53 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json
