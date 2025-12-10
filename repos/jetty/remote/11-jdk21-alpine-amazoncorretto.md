## `jetty:11-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:6a1d9b1bb212accaabe6f65d1d481163bebd75627ca517160cd9ea64b391bbcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:e9127308d9ca9435ddd1e2e3d8854340c924d573fd8ce31c52b7a94e0f475def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188888055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef8bf43edc508ea29a7a396682c80d797aa2efcda27e4e4c28b879253c0ff28`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:06:54 GMT
ARG version=21.0.9.11.1
# Wed, 05 Nov 2025 01:06:54 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:06:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 05 Nov 2025 04:51:40 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 05 Nov 2025 04:51:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 05 Nov 2025 04:51:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 05 Nov 2025 04:51:40 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 05 Nov 2025 04:51:40 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 05 Nov 2025 04:51:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 05 Nov 2025 04:51:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 05 Nov 2025 04:51:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 05 Nov 2025 04:51:40 GMT
WORKDIR /var/lib/jetty
# Wed, 05 Nov 2025 04:51:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 05 Nov 2025 04:51:40 GMT
USER jetty
# Wed, 05 Nov 2025 04:51:40 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 05 Nov 2025 04:51:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Nov 2025 04:51:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d4bc3368d3809cd8ad2e688cb5fe01f46190980ebdbfcac8e9822be3643f0c`  
		Last Modified: Wed, 05 Nov 2025 04:48:38 GMT  
		Size: 161.6 MB (161569892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb6cde75d8cc555b4e8d543bcae34cf885092879519dde171febc69bffab708`  
		Last Modified: Wed, 05 Nov 2025 04:51:57 GMT  
		Size: 23.5 MB (23513835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e48432026ba21b8b81ccf172ef84b6f522722a6bc3437c713702c117729f985`  
		Last Modified: Wed, 05 Nov 2025 04:51:55 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:2e5484051f0c76b6afabcba38276d2723a116bf586b252d2d4ce20721c92f2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b563f1d1fc2e5861ece7613767b34c0a2603ee224b2679fd8126cc8d7fade0fc`

```dockerfile
```

-	Layers:
	-	`sha256:47bcac3d15625b257a1b9367b78a4b9e5f9f8db5213e0a85bed7b9a0e8bedff0`  
		Last Modified: Wed, 05 Nov 2025 06:16:25 GMT  
		Size: 823.3 KB (823325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1860cc063f6be0281979a8935e6f9df7504ee2477d860448eff7bd991ce70895`  
		Last Modified: Wed, 05 Nov 2025 06:16:26 GMT  
		Size: 17.1 KB (17076 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d061be49a67182edc974872db3c526b73b3d99657521ee2fd3471550167d4fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187146552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c5fe749ecfe2e4ac04666904d153b57d6205bcbd52ac1dee21b1dedd37085b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:21 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:16:21 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 04 Nov 2025 23:26:19 GMT
ENV JETTY_VERSION=11.0.26
# Tue, 04 Nov 2025 23:26:19 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 04 Nov 2025 23:26:19 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 04 Nov 2025 23:26:19 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 04 Nov 2025 23:26:19 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 04 Nov 2025 23:26:19 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Tue, 04 Nov 2025 23:26:19 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 04 Nov 2025 23:26:19 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 04 Nov 2025 23:26:19 GMT
WORKDIR /var/lib/jetty
# Tue, 04 Nov 2025 23:26:19 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 04 Nov 2025 23:26:19 GMT
USER jetty
# Tue, 04 Nov 2025 23:26:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 04 Nov 2025 23:26:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 23:26:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fd450f0185222facf50c3585803b24553a293cbfa900eb12641a7831d0da01`  
		Last Modified: Tue, 04 Nov 2025 23:25:34 GMT  
		Size: 159.6 MB (159588499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56078fec94baf92ac74d1b042ba1754838ef2f27b5447ebec3488d87605e389b`  
		Last Modified: Tue, 04 Nov 2025 23:26:35 GMT  
		Size: 23.4 MB (23418107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249daf283281be812311ffc62a581d2aab32fa1b666ae388169d4ebee60a301d`  
		Last Modified: Tue, 04 Nov 2025 23:26:33 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:7293dfd9df472dfe772fccebd46b012651f86ea146565d3f7576210909da6f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.9 KB (839899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d0d77b94a30396928febf92e3d3ac3288e5151db86aff246490030bf6810db`

```dockerfile
```

-	Layers:
	-	`sha256:84eacd267903b5441866a14d7797e040649ab1f595539ad67b575491e384be92`  
		Last Modified: Wed, 05 Nov 2025 00:16:59 GMT  
		Size: 822.7 KB (822732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:976b461ff1e1ea2d99be516d2da7a0efddca9dbcbbbdb76102652ca430081d05`  
		Last Modified: Wed, 05 Nov 2025 00:17:00 GMT  
		Size: 17.2 KB (17167 bytes)  
		MIME: application/vnd.in-toto+json
