## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:99df05430a4038a00ef531e7476a1cf25eba4f1351bc656ac8f3e77e56413646
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:1ec42a28281c2874badc36ae58332dc5412e78c220ee4054f7e6c95abfdb4fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268547463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d0c98adcbdda168e0a6a81c5c4e7d37b2d94faf641fba0caaa9008aed87013`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d89ce34f31bbf0c736abd2c5850a89a70a63c183300873b63c89b857f2347a`  
		Last Modified: Fri, 05 Jul 2024 19:56:48 GMT  
		Size: 165.7 MB (165682730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad2bd1b82a10568c5ab847141430e47dfccadafe2b58030697c6de9bcadbebc`  
		Last Modified: Fri, 05 Jul 2024 20:52:10 GMT  
		Size: 40.2 MB (40216428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24668de818520f9e9760f7bbca4a66d90f5f93b0028dfe5a22aa59b9f25418`  
		Last Modified: Fri, 05 Jul 2024 20:51:51 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:fb2d49f17f8e2230a4a4725650133a87efcd6ae2b839411ca2be0017a3b2d43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6001294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8366e52e6d46fd2d2499c3332d74e67a9d99432949e08788c6c50fb420527d`

```dockerfile
```

-	Layers:
	-	`sha256:aa4ca22c289b10ff44ce32cddd3439784ae31652b9dbd9532c8336ec76fe3f16`  
		Last Modified: Fri, 05 Jul 2024 20:52:09 GMT  
		Size: 6.0 MB (5983202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a17f95bbf1776ef1a1c5ffc52f99c77682b253ed3ca30d99484e66288f6bde5e`  
		Last Modified: Fri, 05 Jul 2024 20:52:11 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5073ac0c999bfc86c227da8be5ed51f2443f8b1f6db306c6a21facf9ccd5c7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268645920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d43d1ab9e9ac77ed3cc255397b2e58febe73f14a6bb26125122493179688cd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4656569e1791b9a2fca54650735b260b09155d4ae7d843f41c8223a93b62836e`  
		Last Modified: Fri, 05 Jul 2024 20:20:44 GMT  
		Size: 163.7 MB (163739172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dc69aa644b785b27db099a0eebb6b97cd591c568922b62390b3b26d8d994c`  
		Last Modified: Fri, 05 Jul 2024 21:00:08 GMT  
		Size: 40.3 MB (40336317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239a84f23b3f810faea95399e03c4c554a0f47be6a073fd3239c708b0d71a87b`  
		Last Modified: Fri, 05 Jul 2024 21:00:06 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:2dd4022ec653b8bd90f08c823f0bf16db465651861910ec20b70e441cf28b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6000390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6c6596726eace04e3788ad8ebeecba2a6acefc61b30442df16bf3d75b48b4`

```dockerfile
```

-	Layers:
	-	`sha256:0cf9cb844ba37cd220088fe2e091a1329e4a32a23f5a3450f4c99f9abce7cad2`  
		Last Modified: Fri, 05 Jul 2024 21:00:07 GMT  
		Size: 6.0 MB (5981865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1923e2d64682cd4a5467e297e57aacae7e5c8deb0d28408789ba17255139b3`  
		Last Modified: Fri, 05 Jul 2024 21:00:06 GMT  
		Size: 18.5 KB (18525 bytes)  
		MIME: application/vnd.in-toto+json
