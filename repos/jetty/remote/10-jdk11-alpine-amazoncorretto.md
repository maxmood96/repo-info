## `jetty:10-jdk11-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:3ca54aa1ed87105cb6735128d6f70ff36556279078d7753de5db8e0dd037af45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:10-jdk11-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:3cda5ee4effb3ef8d4dd821cd30343518c1d8cb474dbef9915acb4c8f13f6c19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163652302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96112cfab00b0dc79e4feee6baa5e4e921aecb70bc71c670c809147ac05bdde5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:33:24 GMT
ARG version=11.0.20.9.1
# Thu, 28 Sep 2023 23:33:31 GMT
# ARGS: version=11.0.20.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Thu, 28 Sep 2023 23:33:32 GMT
ENV LANG=C.UTF-8
# Thu, 28 Sep 2023 23:33:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 28 Sep 2023 23:33:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 29 Sep 2023 04:52:43 GMT
ENV JETTY_VERSION=10.0.16
# Fri, 29 Sep 2023 04:52:44 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 29 Sep 2023 04:52:44 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 29 Sep 2023 04:52:44 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 29 Sep 2023 04:52:44 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 29 Sep 2023 04:52:44 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.16/jetty-home-10.0.16.tar.gz
# Fri, 29 Sep 2023 04:52:44 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 29 Sep 2023 04:52:53 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 29 Sep 2023 04:52:53 GMT
WORKDIR /var/lib/jetty
# Fri, 29 Sep 2023 04:52:53 GMT
COPY multi:04e96d62b43d0ed55ad32900f133ff3fa46502048db2c67b0ea7a783ed3acc37 in / 
# Fri, 29 Sep 2023 04:52:53 GMT
USER jetty
# Fri, 29 Sep 2023 04:52:53 GMT
EXPOSE 8080
# Fri, 29 Sep 2023 04:52:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Sep 2023 04:52:53 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198630ea96142bcc184915dc1faf35392959b5b73b651ed0f644710b394bb6d6`  
		Last Modified: Thu, 28 Sep 2023 23:38:05 GMT  
		Size: 141.4 MB (141375211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd708c12b2083e618ca8a68c1d2640df86d41e169f233834d2e4dfb634fa81d6`  
		Last Modified: Fri, 29 Sep 2023 05:01:46 GMT  
		Size: 18.9 MB (18873503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1458c9d0af4ec2617478cb192a0854b87472083815a269bd9445ecd68b408d8`  
		Last Modified: Fri, 29 Sep 2023 05:01:44 GMT  
		Size: 1.6 KB (1621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
