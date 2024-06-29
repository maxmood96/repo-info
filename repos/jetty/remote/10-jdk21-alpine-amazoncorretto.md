## `jetty:10-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:7c76cb47dd4f715be38c7875b0335120f0813f22bfef2e987940f57dab2679a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:60b810abd936e194474c8a4d634c15c447cbe6ebf35d50d7c51fe199b4756f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182692951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae9a012184ee7fd70ff620c0bc25e5a935092f8f98a28f8113e14aa7b588453`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 31 Jan 2024 21:20:39 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["/bin/sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
ARG version=21.0.3.9.1
# Wed, 31 Jan 2024 21:20:39 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Wed, 31 Jan 2024 21:20:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
WORKDIR /var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
USER jetty
# Wed, 31 Jan 2024 21:20:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c3c30037b360ea1558934aa34c916aa9303537b13bf05accba1f889c8ba6`  
		Last Modified: Thu, 20 Jun 2024 20:47:19 GMT  
		Size: 159.9 MB (159874477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95086ffda7b5611afae9b3bb485e69ec7e19e957868192340b53eee6951da9f0`  
		Last Modified: Fri, 28 Jun 2024 20:57:42 GMT  
		Size: 19.4 MB (19399476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773ad3baa223f79cc634f1989347bbd7522459487d5bac7068ff04ace4fdcc63`  
		Last Modified: Fri, 28 Jun 2024 20:57:41 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:83b75e3ab4bb0e3c483970f4a097d2c1dcbf6aeb567f9bac6deeedc3e09632cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.2 KB (703207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1532d5ab8ac3675f92a0b03c1d8366905bd31907d68c12c924faaaad49880b`

```dockerfile
```

-	Layers:
	-	`sha256:b460686f51cd9b0c4ef2ee6e3b0e9b49764f7fff2c35b990c390c441b1bf086e`  
		Last Modified: Fri, 28 Jun 2024 20:57:41 GMT  
		Size: 686.3 KB (686258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8a1356471f56674fd405af294d3337f86d092035bd0c8401a3441198829b7b`  
		Last Modified: Fri, 28 Jun 2024 20:57:41 GMT  
		Size: 16.9 KB (16949 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:248aab6f0dcd5777a3b945132a1ca724530d6a327e548d33c7e763de1c170474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180201624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4b93cebeb34d2ff36c7754548f1e8764f29541ffb047c276e2cfb2af828521`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 31 Jan 2024 21:20:39 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["/bin/sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
ARG version=21.0.3.9.1
# Wed, 31 Jan 2024 21:20:39 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Wed, 31 Jan 2024 21:20:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
WORKDIR /var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
USER jetty
# Wed, 31 Jan 2024 21:20:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a2aa088d379d737e12a65d06b983e32465ccd5a65c1f193aa72e5f7b342dae`  
		Last Modified: Wed, 26 Jun 2024 16:54:53 GMT  
		Size: 157.4 MB (157387095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee89916e56dee46e45ca95d2f59fe61398879e36f3bd886287e0b49b6c0473`  
		Last Modified: Fri, 28 Jun 2024 21:25:26 GMT  
		Size: 19.5 MB (19455661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb979b0d5145e485a8ae708627d15ec47a05b5db8879f89c2f3681d5c2d52eb`  
		Last Modified: Fri, 28 Jun 2024 21:25:25 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8839cf19e5d7afadeddbbe01befbe36eeb9bd812b009b6fd6fe3f85145559965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 KB (702914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113f27feea6627c0c97b454e7edf72fb056dc4b8ab57a294d8b50fb8f2e12d30`

```dockerfile
```

-	Layers:
	-	`sha256:b582fbea24574f48f30ed3d39116d1d2fb9f29b915ef916b93887d697a5f733b`  
		Last Modified: Fri, 28 Jun 2024 21:25:25 GMT  
		Size: 685.7 KB (685664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff3a02763d576b6f50c4271639c1d3ab476318bbb6a87e26c87cb24d0a952414`  
		Last Modified: Fri, 28 Jun 2024 21:25:25 GMT  
		Size: 17.2 KB (17250 bytes)  
		MIME: application/vnd.in-toto+json
