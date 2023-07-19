## `jetty:11-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:9e8c7321bdabaa0ecd747b2ed8e82d2556427760653a53a49b2ad75509ea2657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:11-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d53b729085a6b45bce45548f508a41130faf93fccb460a395d860431ad666424
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171487709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104057d201526a2d73d81ca45daee00f1e1c47ee8b6916ee2fa7fdf15f3c392`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 19 Jul 2023 00:30:39 GMT
ARG version=17.0.8.7.1
# Wed, 19 Jul 2023 00:30:44 GMT
# ARGS: version=17.0.8.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip
# Wed, 19 Jul 2023 00:30:45 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jul 2023 00:30:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jul 2023 00:30:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 19 Jul 2023 01:07:08 GMT
ENV JETTY_VERSION=11.0.15
# Wed, 19 Jul 2023 01:07:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 19 Jul 2023 01:07:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 19 Jul 2023 01:07:08 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 19 Jul 2023 01:07:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 19 Jul 2023 01:07:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Wed, 19 Jul 2023 01:07:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 19 Jul 2023 01:07:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 19 Jul 2023 01:07:19 GMT
WORKDIR /var/lib/jetty
# Wed, 19 Jul 2023 01:07:19 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Wed, 19 Jul 2023 01:07:19 GMT
USER jetty
# Wed, 19 Jul 2023 01:07:19 GMT
EXPOSE 8080
# Wed, 19 Jul 2023 01:07:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Jul 2023 01:07:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c903d65f836bac1d2c7226b4beb71e6515b02e680e1428019b18aeed583279`  
		Last Modified: Wed, 19 Jul 2023 00:46:03 GMT  
		Size: 145.7 MB (145738113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b682d0b625b0c37f5eeb562ebe1412a7b35fdcf9290a60b5371d7c9c9a307d4e`  
		Last Modified: Wed, 19 Jul 2023 01:14:11 GMT  
		Size: 22.4 MB (22350104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46721affa23a7447a5db1219a90622dec9c577a2f63cbf6ca533f20706789203`  
		Last Modified: Wed, 19 Jul 2023 01:14:09 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
