## `jetty:9-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:6385d28a7afd009a65af51603c632793dcdf1ffeb65531ba6f121518441ce95c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:eec8c9188223212789955590c20333daa545d5fd7aa62e11aff95554bceaaefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181582707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa487d10fd832fd8519243ee2fb1083240ab537bf92c8309f6f681fd16466f46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 14 Jan 2025 05:07:03 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
ARG version=21.0.6.7.1
# Tue, 14 Jan 2025 05:07:03 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
WORKDIR /var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
USER jetty
# Tue, 14 Jan 2025 05:07:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d56f35012a0efb0cf3144f926e650140b492ee84050727c5057e3319c49c1db`  
		Last Modified: Fri, 14 Feb 2025 20:34:52 GMT  
		Size: 159.0 MB (158955298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7626b5a3b2493c186a6449ae9851b15eb67b89edfb12c28e15442aa6a0fd967`  
		Last Modified: Sat, 15 Feb 2025 09:54:50 GMT  
		Size: 19.0 MB (18983470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47045df60ddd9a85626c7134ca3d3fd830cf9028fd8b652ad1cb88e890d911a1`  
		Last Modified: Sat, 15 Feb 2025 09:54:49 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:4aa63a7e6a09d8950dec3af93a9014a106691afebcdc647e64fd4dd35bf0b0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.9 KB (619949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec24a319caeafe662e3760ce691847cf8331c65858fd754601684f3a71e5cac`

```dockerfile
```

-	Layers:
	-	`sha256:37f10ad881d25bed56db7b480774d24ab05556034b8a93038bfc3b4d72735fd9`  
		Last Modified: Sat, 15 Feb 2025 00:19:55 GMT  
		Size: 602.8 KB (602800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0fc13270a62d75410be667b2806e78c7fdecf4f4707636b4cff4b40ee514987`  
		Last Modified: Sat, 15 Feb 2025 00:19:56 GMT  
		Size: 17.1 KB (17149 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:8bf4a834812d77781af169098252e8550c524f25413125246e8b8954cfb1d4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179813019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cdc539323b2215b8ebc6154f8c337e21d2d5279dc213dbbc5640b3395a8073`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 14 Jan 2025 05:07:03 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
ARG version=21.0.6.7.1
# Tue, 14 Jan 2025 05:07:03 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
WORKDIR /var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
USER jetty
# Tue, 14 Jan 2025 05:07:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e191a064c87c1670d74b11fad78096a8c5d30bbd31d3e71b3dbe4d032af4cdaa`  
		Last Modified: Sat, 15 Feb 2025 01:52:31 GMT  
		Size: 156.9 MB (156935312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0cf3743990d06f6fd298cccd67df26ed0884687bb3442614e39c895287d3a5`  
		Last Modified: Sun, 16 Feb 2025 12:07:15 GMT  
		Size: 18.9 MB (18882986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f1d3c815ab606ca279ab4185761fdb4ab275b35c5046e6f622bf0e258dcc0`  
		Last Modified: Sun, 16 Feb 2025 12:07:17 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:6944e77f1ffb6a1929aa099ef48d2b0eb2e41824b17fc2409e73869ad5d856af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.4 KB (619448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f66c0645afe5eed72da5cb20633c09dedd82dc8b0174bd4e66221817e789a8`

```dockerfile
```

-	Layers:
	-	`sha256:a7895e58084345a026a5e7329e0f06e576938a591b769c288caffbc01b01709e`  
		Last Modified: Sat, 15 Feb 2025 09:17:45 GMT  
		Size: 602.2 KB (602207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199ee5562d9e37788b869b54fc7a3e3691dfeb04b39bb7d1eaebd934e4d763a6`  
		Last Modified: Sat, 15 Feb 2025 09:17:46 GMT  
		Size: 17.2 KB (17241 bytes)  
		MIME: application/vnd.in-toto+json
