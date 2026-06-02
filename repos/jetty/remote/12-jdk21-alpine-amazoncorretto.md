## `jetty:12-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:0c0ef6ff521418bd489ca13938a0229e7f62082215726dea724b351c13167bef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:21cbe449104fe12ec71995130c28de61b75f4292c5368733fd708605008b971c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220679888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89797c4e6a5eb51be23cb859c559f27ebf7a7c3d4308d2415093e6c9f9a7d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:52 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:52 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 02 Jun 2026 17:56:37 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 02 Jun 2026 17:56:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 Jun 2026 17:56:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 Jun 2026 17:56:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 Jun 2026 17:56:37 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 02 Jun 2026 17:56:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 02 Jun 2026 17:56:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 Jun 2026 17:56:37 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 02 Jun 2026 17:56:37 GMT
WORKDIR /var/lib/jetty
# Tue, 02 Jun 2026 17:56:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 02 Jun 2026 17:56:37 GMT
USER jetty
# Tue, 02 Jun 2026 17:56:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 17:56:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 17:56:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248b05a9ca5f91c177d0decf2d392d42cc189cd2cf569e6cdb0fd2b734d669bb`  
		Last Modified: Wed, 22 Apr 2026 21:35:12 GMT  
		Size: 161.8 MB (161813161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b9a8786b99c753ab9ba9bcfd4f9ccd26be3a45b7a73a2ff260137aabbc2329`  
		Last Modified: Tue, 02 Jun 2026 17:56:48 GMT  
		Size: 55.0 MB (55000664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e428d3ded32777a2a150ac55f073abbbf7b0c99cce0eb767bffe9cd2b5671256`  
		Last Modified: Tue, 02 Jun 2026 17:56:46 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:4a732a93771d00b6f55b2f5483c584f4d426e4bf571ec9a76d5bb63ffd13c0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1030034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29811ca784c39ca83a1a27c97c344dd9f729619e9bd88db931dff1980ac3aae3`

```dockerfile
```

-	Layers:
	-	`sha256:d580e47ec1613f8e69f87c0e5825cd428387a21e21d5160917a1c4395f8a21cf`  
		Last Modified: Tue, 02 Jun 2026 17:56:47 GMT  
		Size: 1.0 MB (1012959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442fcd84976beb00f8e784a540cc216f13582bdc4d86237b55a6b2abf50462d0`  
		Last Modified: Tue, 02 Jun 2026 17:56:46 GMT  
		Size: 17.1 KB (17075 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:7f8ca7ee74e8f3a65fc98f822d20776f05f9cc1af4a96263c41345d538106637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218921181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfc7aa5212058cbd3d852f5133d26d6818c23f9bdb05c794cf5e44ad0330c92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:45 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:45 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:45 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 02 Jun 2026 17:55:36 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 02 Jun 2026 17:55:36 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 Jun 2026 17:55:36 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 Jun 2026 17:55:36 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 Jun 2026 17:55:36 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 02 Jun 2026 17:55:36 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 02 Jun 2026 17:55:36 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 Jun 2026 17:55:36 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 02 Jun 2026 17:55:36 GMT
WORKDIR /var/lib/jetty
# Tue, 02 Jun 2026 17:55:36 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 02 Jun 2026 17:55:36 GMT
USER jetty
# Tue, 02 Jun 2026 17:55:36 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 17:55:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 17:55:36 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ecb8ee1bb766b7846294cccb87c572391bd352b362a7867597720dd8b7df36`  
		Last Modified: Wed, 22 Apr 2026 21:35:04 GMT  
		Size: 159.8 MB (159828502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b173cae41a94c403e0b4f320622da474e2bd88dd32bcf781f929f6125e808e1`  
		Last Modified: Tue, 02 Jun 2026 17:55:47 GMT  
		Size: 54.9 MB (54890935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464a78322a4b00e700b7215a13aac8a80207baa6f0654166beb2b9ce0667db8e`  
		Last Modified: Tue, 02 Jun 2026 17:55:45 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:914ff6536f3a53a1291eb2ca2ea31f4335452247c51c13af9a3922e8cace6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1028883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9324bf2e6513b4374d6d7eaa67bc8bdd978e9fde461aa8188e6fd7895ae66f`

```dockerfile
```

-	Layers:
	-	`sha256:b4cf5ddd934ead5c248e57b84a1b66a8a12bc0f766f05c25c2eba9cca5e3a948`  
		Last Modified: Tue, 02 Jun 2026 17:55:46 GMT  
		Size: 1.0 MB (1011716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:695bd3af3b63cb31797827f7f663169abac5c461859495a4cad342c76c5ac124`  
		Last Modified: Tue, 02 Jun 2026 17:55:45 GMT  
		Size: 17.2 KB (17167 bytes)  
		MIME: application/vnd.in-toto+json
