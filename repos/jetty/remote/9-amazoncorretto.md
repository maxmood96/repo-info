## `jetty:9-amazoncorretto`

```console
$ docker pull jetty@sha256:5a2ce061dec769d9ac338b9145797df8cd16c6c0d370e14115dcb70f0986db63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:60fb6a66e8afbbe0f3aa08e96a6ec8d4d8a0c466cf5f52ec5af44d89b05e412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243556426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a52e1098eb96afb130e8d3b494c55960666367a217b197bf62b0cac044b548c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 09 Sep 2024 08:47:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 08:47:04 GMT
ARG version=21.0.5.11-1
# Mon, 09 Sep 2024 08:47:04 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
WORKDIR /var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
USER jetty
# Mon, 09 Sep 2024 08:47:04 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Sep 2024 08:47:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938187b8d043d01191d993a4f830d347d069880d972a1ce7b14660c4fb5460dd`  
		Last Modified: Wed, 16 Oct 2024 17:57:46 GMT  
		Size: 164.8 MB (164785975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c92015322bd4eae70ee59cb2fc2433c7dfae9950479e09e32399f67b81c048`  
		Last Modified: Wed, 16 Oct 2024 19:00:20 GMT  
		Size: 16.1 MB (16090629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b109507abe0c1f93c842d1ba4747e150da1310e13fed05464d6cbcef9eb50ecd`  
		Last Modified: Wed, 16 Oct 2024 19:00:19 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e5562404a1007c9488fdb4b3cae5b179329286375448624d0367e1563cb2fd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5924449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c22bccce6c81d78cdfec31682985e7c08a113663a3192ab24281c3db638937`

```dockerfile
```

-	Layers:
	-	`sha256:8c65f2037fe69a21e299b773d0dd67ea22d837e04195e61c3fef085e9fbef5d5`  
		Last Modified: Wed, 16 Oct 2024 19:00:19 GMT  
		Size: 5.9 MB (5906288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed758e8d6ce5dec0a5e522a38c9b768a285a44b5d4416214367bcf784ecd20e6`  
		Last Modified: Wed, 16 Oct 2024 19:00:19 GMT  
		Size: 18.2 KB (18161 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:89f8157fa3376581fa06f3fcbdf4ec0914a798f0590a76969298930c8e054dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243647346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f02582cb5fe7fac4511d518c3bd43dd488b63c047c4f176d7f7b26f8716f7f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 09 Sep 2024 08:47:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 08:47:04 GMT
ARG version=21.0.5.11-1
# Mon, 09 Sep 2024 08:47:04 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
WORKDIR /var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
USER jetty
# Mon, 09 Sep 2024 08:47:04 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Sep 2024 08:47:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36748b1b7eead6ad7801319a0c510e15a241d9098d75d4df217e6b5a28c08099`  
		Last Modified: Wed, 16 Oct 2024 18:31:48 GMT  
		Size: 162.8 MB (162840504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927bcc0930395cf0276da80d2a5024b1c39b8d02c434edee6c4e9a3b844efe2f`  
		Last Modified: Wed, 16 Oct 2024 19:57:35 GMT  
		Size: 16.2 MB (16212517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3483bbff9c10642ddbd3eb15b022691591c03502252e2bdf9ff2cc69e7dd014b`  
		Last Modified: Wed, 16 Oct 2024 19:57:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3ae28ec0ed5b082fad55a9a94138c7f680a7bc8180ede608d8a1447fc7ecf690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d50d95d2c621708adaca49bb408c622f97a9f7fb815aae45c6c26660ef7e850`

```dockerfile
```

-	Layers:
	-	`sha256:dffabf239b45fdd0a4e6bec0b103b4519a3ab3c253c92e4de6375fb5b82adb46`  
		Last Modified: Wed, 16 Oct 2024 19:57:35 GMT  
		Size: 5.9 MB (5904951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74af989aa57092de3c30ccf430c6a8ce56848edef744bab49b79f0b9f37546a5`  
		Last Modified: Wed, 16 Oct 2024 19:57:34 GMT  
		Size: 18.3 KB (18289 bytes)  
		MIME: application/vnd.in-toto+json
