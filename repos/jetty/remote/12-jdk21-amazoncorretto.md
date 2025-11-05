## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:be442fc8b297484ca5ffdd0c972e73df1de544b365b995ba6a850b4d38fef897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:b8896a52a7e940c203e747ee3527eff8b398b96f6f3205dfb8d2b3ee5e007aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280365991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d877acbf4e4accbaa57a6c195d6e794673b0ca23a873d169a3a6fed0c538bd73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:25 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:25 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:13:02 GMT
ENV JETTY_VERSION=12.1.3
# Fri, 31 Oct 2025 01:13:02 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:13:02 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:13:02 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:13:02 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:13:02 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Fri, 31 Oct 2025 01:13:02 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:13:02 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:13:02 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:13:02 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:13:02 GMT
USER jetty
# Fri, 31 Oct 2025 01:13:02 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:13:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:13:02 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b8bf1a2d41e5961e041978e350f514e0b16151864da2fa18fedc6f348e6f0f`  
		Last Modified: Fri, 31 Oct 2025 01:11:23 GMT  
		Size: 165.5 MB (165482592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c29e70ad6a793a4efebbca2f79cd4e0fa9b61dc9a5ac9a082d8d327d17f1fa7`  
		Last Modified: Fri, 31 Oct 2025 01:13:30 GMT  
		Size: 51.9 MB (51947455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f188c3f54838eaffbb32cbc932f5140041044e38f9ef2b3c10dc8f9db50dbd`  
		Last Modified: Fri, 31 Oct 2025 01:13:22 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:705a7cfb31573fa559bcf9307974c745304b4f45828c8988794c9737ca53a32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6171149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8691a579936c72a2d98214113424d3bd4d54df34ef278ee5e3f649d504b1c4`

```dockerfile
```

-	Layers:
	-	`sha256:9176ce4ed8e99417ebfeadc02652c7023d7cc11ff19a5c8d3b5d47bda43300be`  
		Last Modified: Fri, 31 Oct 2025 02:17:43 GMT  
		Size: 6.2 MB (6152830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ac9d0db9038f47eb825ef30ef7a6d82c97b5d52686764aa274c5294caba658d`  
		Last Modified: Fri, 31 Oct 2025 02:17:43 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:4383c4f2e24558d1c1dc9305a34bc772e00cb7de8e429d89d7769cb9c45a066a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280385013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077b62f511c4ba240279030a0f78852bc7e631f89fae90a0b22e46366a463c43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:12:18 GMT
ARG version=21.0.9.11-1
# Tue, 04 Nov 2025 23:12:18 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 04 Nov 2025 23:12:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:12:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Nov 2025 23:26:22 GMT
ENV JETTY_VERSION=12.1.3
# Tue, 04 Nov 2025 23:26:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 04 Nov 2025 23:26:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 04 Nov 2025 23:26:22 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 04 Nov 2025 23:26:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:26:22 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Tue, 04 Nov 2025 23:26:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 04 Nov 2025 23:26:22 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 04 Nov 2025 23:26:22 GMT
WORKDIR /var/lib/jetty
# Tue, 04 Nov 2025 23:26:22 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 04 Nov 2025 23:26:22 GMT
USER jetty
# Tue, 04 Nov 2025 23:26:22 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 04 Nov 2025 23:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 23:26:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad0d1fcc61302619a93c14ea37d679d5cc2a8f138552caa19924202526997b`  
		Last Modified: Tue, 04 Nov 2025 23:26:04 GMT  
		Size: 163.6 MB (163582941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d671400ad55e4044ffae4c241c3932c566830c127dc2fe053daca7c389b062`  
		Last Modified: Tue, 04 Nov 2025 23:26:50 GMT  
		Size: 52.0 MB (52006738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bbd160994ca797a202cd0d9f73e35fa418f7f4dd67c285a3712013e6438f9d`  
		Last Modified: Tue, 04 Nov 2025 23:26:44 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1d18dbc30d606b44d11f33b7c5a5238770a75f7e97765f3033a0ad13e17b87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba1ec4906c9d264ea2207db023d73e020365a1a3d853822aaebcc64c70dc399`

```dockerfile
```

-	Layers:
	-	`sha256:a406533e8d98b951d79dce802c16fb7cab1dce55c1e86a84adcfa23154de419a`  
		Last Modified: Wed, 05 Nov 2025 00:17:51 GMT  
		Size: 6.2 MB (6151495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1f8ec4c10320d7dcd5d16cce493deee5f50503af9b6daa004819dc9991916e7`  
		Last Modified: Wed, 05 Nov 2025 00:17:52 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json
