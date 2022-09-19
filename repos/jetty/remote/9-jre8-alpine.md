## `jetty:9-jre8-alpine`

```console
$ docker pull jetty@sha256:4bb24b3a3f037f6f384580a39cf2688816bb0476d0d0649d355c28ef258f9884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:9-jre8-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:c8caf9c199a520a5fb311def6ee4fbe694b754d70e8525de95001c724c8ee7f2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67159028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e8ba64d374b2299396eadde391e803eee9df74c67baccb27d67b4c7d03d51e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 11 May 2019 00:07:03 GMT
ADD file:a86aea1f3a7d68f6ae03397b99ea77f2e9ee901c5c59e59f76f93adbb4035913 in / 
# Sat, 11 May 2019 00:07:03 GMT
CMD ["/bin/sh"]
# Sat, 11 May 2019 01:32:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 May 2019 01:32:12 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 11 May 2019 01:32:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Sat, 11 May 2019 01:32:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Sat, 11 May 2019 01:32:32 GMT
ENV JAVA_VERSION=8u212
# Sat, 11 May 2019 01:32:32 GMT
ENV JAVA_ALPINE_VERSION=8.212.04-r0
# Sat, 11 May 2019 01:32:36 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 11 May 2019 04:11:17 GMT
RUN addgroup -S jetty && adduser -D -S -H -G jetty jetty && rm -rf /etc/group- /etc/passwd- /etc/shadow-
# Sat, 11 May 2019 04:11:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 11 May 2019 04:11:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Sat, 11 May 2019 04:11:18 GMT
RUN mkdir -p "$JETTY_HOME"
# Sat, 11 May 2019 04:11:18 GMT
WORKDIR /usr/local/jetty
# Sat, 11 May 2019 04:11:19 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Sat, 11 May 2019 04:11:19 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Sat, 11 May 2019 04:11:19 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Sat, 11 May 2019 04:11:23 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps gnupg curl 		&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvzf jetty.tar.gz 	&& mv jetty-home-$JETTY_VERSION/* ./ 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -fr jetty-home-$JETTY_VERSION/ 		&& apk del .build-deps 	&& rm -fr .build-deps 	&& rm -rf /tmp/hsperfdata_root
# Sat, 11 May 2019 04:11:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 11 May 2019 04:11:24 GMT
RUN mkdir -p "$JETTY_BASE"
# Sat, 11 May 2019 04:11:24 GMT
WORKDIR /var/lib/jetty
# Sat, 11 May 2019 04:11:26 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Sat, 11 May 2019 04:11:26 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 11 May 2019 04:11:27 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Sat, 11 May 2019 04:11:27 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Sat, 11 May 2019 04:11:27 GMT
USER jetty
# Sat, 11 May 2019 04:11:27 GMT
EXPOSE 8080
# Sat, 11 May 2019 04:11:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 May 2019 04:11:28 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:e7c96db7181be991f19a9fb6975cdbbd73c65f4a2681348e63a141a2192a5f10`  
		Last Modified: Sat, 11 May 2019 00:07:31 GMT  
		Size: 2.8 MB (2757034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f910a506b6cb1dbec766725d70356f695ae2bf2bea6224dbe8c7c6ad4f3664a2`  
		Last Modified: Sat, 11 May 2019 01:36:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6abafe80f63b02535fc111df2ed6b3c728469679ab654e03e482b6f347c9639`  
		Last Modified: Sat, 11 May 2019 01:37:30 GMT  
		Size: 54.9 MB (54935634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9cfea88c1061075f5107d1b7b0b822028c1ae74663d83a648231d3566c8b27`  
		Last Modified: Sat, 11 May 2019 04:12:06 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8144bebd7d1bf6d5bc7b3b39b76bcc2f858725bab042dceab012618dc33d0015`  
		Last Modified: Sat, 11 May 2019 04:12:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44499f7897772fc19c5a3bbb14edb8a6f222acc52c62bd7c3ed0ff3238a40389`  
		Last Modified: Sat, 11 May 2019 04:12:06 GMT  
		Size: 9.5 MB (9461244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea5e9998f9af22a825abab8cb7067b9c6ff0fddf4951fff01738f57da2ddcd5`  
		Last Modified: Sat, 11 May 2019 04:12:05 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1824780cfd0166b3661eba93e6281c0ecd34735372cc574010dfdd424a82036`  
		Last Modified: Sat, 11 May 2019 04:12:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbaaf56a0bdf1cdf548a9f5cd85b50786e0760d9418a3d78b583331d3164e4c`  
		Last Modified: Sat, 11 May 2019 04:12:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7741ca9610f12eeed61e6def7fdaa08d66461ac6ebb19cca7befcc9faa719170`  
		Last Modified: Sat, 11 May 2019 04:12:05 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
