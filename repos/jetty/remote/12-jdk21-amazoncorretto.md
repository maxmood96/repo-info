## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:bb4ce6391ee72658eedc8d82e3b7664731f7fb100fdf768c98ef569b8713fa50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:7c1cf407199c8379d90b78ff3d4161d77aa6c15f8cded3cec910d194fb103402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280381199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7f0d12d27b9054b8cb9425a1f7d7ab867324dff99214d95c4dec23e894ee73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:21 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:23:21 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:23:21 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:13:15 GMT
ENV JETTY_VERSION=12.1.3
# Wed, 03 Dec 2025 21:13:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 03 Dec 2025 21:13:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 03 Dec 2025 21:13:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 03 Dec 2025 21:13:15 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 21:13:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Wed, 03 Dec 2025 21:13:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 03 Dec 2025 21:13:15 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 03 Dec 2025 21:13:15 GMT
WORKDIR /var/lib/jetty
# Wed, 03 Dec 2025 21:13:15 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 03 Dec 2025 21:13:15 GMT
USER jetty
# Wed, 03 Dec 2025 21:13:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 03 Dec 2025 21:13:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Dec 2025 21:13:15 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb2013f839dc1b3c014b823b3aac80d0e6d67fac06ba1b5ce16eef96069369`  
		Last Modified: Wed, 03 Dec 2025 21:11:38 GMT  
		Size: 165.5 MB (165496684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07153dab895156a45590b9ad4481b77d632f3850ba023700d0cc5750b502bf2`  
		Last Modified: Wed, 03 Dec 2025 21:13:37 GMT  
		Size: 52.0 MB (51952067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333fdd1589e679221d0aafce1665e33332312c5dc30ace7fd4bee80796de6e6c`  
		Last Modified: Wed, 03 Dec 2025 21:13:33 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e2b2d49b8ebb4137053a8c96513398f28402e93c7fc43d8a71e0912db933d06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6171153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d929de95d94519a3a12646537027dd59ece6dce978e5e8349c5b9c5aada2a0`

```dockerfile
```

-	Layers:
	-	`sha256:2856b653bb470303f56d44308e9412847525cdbc1e69394ea405da9baaf4a025`  
		Last Modified: Thu, 04 Dec 2025 00:17:44 GMT  
		Size: 6.2 MB (6152834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937f11e9f046226353e7b8407de4ed2e71929569e5e1a0e14e19276ce85ed004`  
		Last Modified: Thu, 04 Dec 2025 00:17:45 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:de806ff105704948d6a4e1f6951ba963ddb2d68df4993ed3ea47131ec3517e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280384036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb5e95f7d9556ca814a8bde7815e9c7839629dac4931d49d122cabeed33ce46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:26 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:26 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:27:26 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:13:57 GMT
ENV JETTY_VERSION=12.1.3
# Wed, 03 Dec 2025 21:13:57 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 03 Dec 2025 21:13:57 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 03 Dec 2025 21:13:57 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 03 Dec 2025 21:13:57 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 21:13:57 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Wed, 03 Dec 2025 21:13:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 03 Dec 2025 21:13:57 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 03 Dec 2025 21:13:57 GMT
WORKDIR /var/lib/jetty
# Wed, 03 Dec 2025 21:13:57 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 03 Dec 2025 21:13:57 GMT
USER jetty
# Wed, 03 Dec 2025 21:13:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 03 Dec 2025 21:13:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Dec 2025 21:13:57 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ba2b3f44053754feffb2ec7cfa45b66127e117d0d28e5607dbc6e1b6044b97`  
		Last Modified: Wed, 03 Dec 2025 21:41:24 GMT  
		Size: 163.6 MB (163582881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9af9e43dca74baa44042a3dd80a61b271f7c120e87ab62fa1c2244cd2a08114`  
		Last Modified: Wed, 03 Dec 2025 21:14:23 GMT  
		Size: 52.0 MB (52006478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34003cec7899a9a9be42b643345f92c7c6fdad87a3e71992ba31e620ae5f0ee0`  
		Last Modified: Wed, 03 Dec 2025 21:14:17 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ab6236b6bf40827fd01791ef08acd67a271d7b2b4b74e585b2c13361f268b186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5210e6668d0e475422c956962fdfe9ecc7d134c2fc9120fffc854ae0d1c783d5`

```dockerfile
```

-	Layers:
	-	`sha256:053c1481abad1d0502f21fda78950ba2a344e8c09b54899ec2fc119e59805768`  
		Last Modified: Thu, 04 Dec 2025 00:17:51 GMT  
		Size: 6.2 MB (6151499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edca8b5db0fe2374265942aa27c01162df92d4dd5e2752f8abdf2a3e99300105`  
		Last Modified: Thu, 04 Dec 2025 00:17:52 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json
