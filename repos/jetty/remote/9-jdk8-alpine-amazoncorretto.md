## `jetty:9-jdk8-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:43cdfb8290d3ebf20b7db85db54ad658ab9236725e41500f726b2d75cfd814fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:9-jdk8-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:16370878864a174a90a939463243d930e38b99d82b5b7d0cdd80bf5efb109f89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121267363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046482a6a6be775ad3db3c925ffbd72192d35e4671bc43f960c75ff63a2f7140`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 19 Jul 2023 00:22:54 GMT
ARG version=8.382.05.1
# Wed, 19 Jul 2023 00:22:58 GMT
# ARGS: version=8.382.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip
# Wed, 19 Jul 2023 00:22:58 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jul 2023 00:22:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jul 2023 00:22:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 19 Jul 2023 01:05:12 GMT
ENV JETTY_VERSION=9.4.51.v20230217
# Wed, 19 Jul 2023 01:05:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 19 Jul 2023 01:05:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 19 Jul 2023 01:05:12 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 19 Jul 2023 01:05:12 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 19 Jul 2023 01:05:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.51.v20230217/jetty-home-9.4.51.v20230217.tar.gz
# Wed, 19 Jul 2023 01:05:13 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 19 Jul 2023 01:05:22 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 19 Jul 2023 01:05:22 GMT
WORKDIR /var/lib/jetty
# Wed, 19 Jul 2023 01:05:22 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Wed, 19 Jul 2023 01:05:22 GMT
USER jetty
# Wed, 19 Jul 2023 01:05:22 GMT
EXPOSE 8080
# Wed, 19 Jul 2023 01:05:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Jul 2023 01:05:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9a5290ca476867a1562e1e77b6515f23464bd97009f0233d7df46f6ac66b19`  
		Last Modified: Wed, 19 Jul 2023 00:37:18 GMT  
		Size: 100.1 MB (100057189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf6dfb2d32512f83c712bc4fdbb0134be46b7e7a399afb441d7875cebde9bcd`  
		Last Modified: Wed, 19 Jul 2023 01:12:54 GMT  
		Size: 17.8 MB (17810682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6478dcad3ccf9e70838bc2c854575fd9c32bfaddb85be35cf650c5390a1d4789`  
		Last Modified: Wed, 19 Jul 2023 01:12:53 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
