## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:ac460ee9e37f6dd22498049f4be7bbcf849f7a845f9e5228dbdd5624d067f9ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:2b122c2e36adc2345a0923fd9a26bc0b83fe784f7b3536c201593a8cab3178b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230384238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e503ac5d98c948b4a3f4c41851436854daa6d47d98f8441df867d23bc91362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Dec 2024 01:30:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
USER jetty
# Wed, 04 Dec 2024 01:30:10 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Dec 2024 01:30:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Dec 2024 01:30:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce47bbf12c856f2c3827f5733bc33beb2ba86473a4817f4f8c1b87f1990cd6d`  
		Last Modified: Sat, 16 Nov 2024 00:48:47 GMT  
		Size: 151.6 MB (151607405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a7c7f315518a13c887f937adb3647f57137651732f411e1ba2d0bf754df5bf`  
		Last Modified: Wed, 04 Dec 2024 20:28:18 GMT  
		Size: 16.1 MB (16097728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd28508921c2cc7bb7495e9b3bb4a6955f9a69f146a08c36109776c66baa10b`  
		Last Modified: Wed, 04 Dec 2024 20:28:17 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:fb24e48357e8a96c2c9ebd59e9bc89f101c1737ce55303d5107f80368bbe3c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5930267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa7c9c9d5920fd866cee5ba215e548716c47e6c777c0e0d9b89653ae68322cc`

```dockerfile
```

-	Layers:
	-	`sha256:da6315509fd0076f69ce9c1cbe653f8cf09749f926ceb24c17a9fa4b04e167e1`  
		Last Modified: Wed, 04 Dec 2024 20:28:17 GMT  
		Size: 5.9 MB (5912836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4734d5d3894f874aa996f69be478948ff75d3b09656bad8c9f1a975c81162f0`  
		Last Modified: Wed, 04 Dec 2024 20:28:17 GMT  
		Size: 17.4 KB (17431 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:903bf3c1f7766ffd3b2d77200976557c70800b7e6ea322bb91207a4929ff3b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231020744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea12361d3440eeeb5dced9df35934c59642ced490c2ca79d7127dc0439660b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Dec 2024 01:30:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
USER jetty
# Wed, 04 Dec 2024 01:30:10 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Dec 2024 01:30:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Dec 2024 01:30:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737939e85848b34826899ab042c8aad6fc1fba8f7f661936f213981c4b20421e`  
		Last Modified: Sat, 16 Nov 2024 00:58:26 GMT  
		Size: 150.2 MB (150238943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5f7d14c816f806402adba231132b059f28a2f6d15c038cc70b389b6daad927`  
		Last Modified: Wed, 04 Dec 2024 20:36:29 GMT  
		Size: 16.2 MB (16198248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc04f407607e174efb4d34bbcb109b2486407ac27a4d826267cde7252cf46b32`  
		Last Modified: Wed, 04 Dec 2024 20:36:28 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5b0e63bba427cbfe2ed4547caab717e17679dc97d7d40e6d1d1da6679e3325aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5928986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febdd585958c5df9efa4d9432d15c9aef6dd9fed76b183b32e783b7b3e1cf555`

```dockerfile
```

-	Layers:
	-	`sha256:1d9857ab7071cc154f206b6891b10e243a96008bb7cbc6c5b69afb9b6003538e`  
		Last Modified: Wed, 04 Dec 2024 20:36:29 GMT  
		Size: 5.9 MB (5911463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11e542e51035cde275a793886b50337b7c153c8ed29cd604a5673827dadbe7`  
		Last Modified: Wed, 04 Dec 2024 20:36:29 GMT  
		Size: 17.5 KB (17523 bytes)  
		MIME: application/vnd.in-toto+json
