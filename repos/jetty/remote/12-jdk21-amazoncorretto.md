## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:b590211c02008b655d087f78e44ebf869d1b818dc974e99f53755ddcbae43751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:68da772f9afe424406e3c4b470b7f2047ce1eaf1949b3e65bedd93a58887c49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280571990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8cda7f0c31c2e7c3e54ebf9111c8fbc6db8458948006cf54073b8203779d3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:26 GMT
ARG version=21.0.10.7-1
# Tue, 27 Jan 2026 22:13:26 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:13:26 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Jan 2026 23:13:45 GMT
ENV JETTY_VERSION=12.1.5
# Tue, 27 Jan 2026 23:13:45 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Jan 2026 23:13:45 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Jan 2026 23:13:45 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Jan 2026 23:13:45 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:13:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Tue, 27 Jan 2026 23:13:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Jan 2026 23:13:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 27 Jan 2026 23:13:45 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Jan 2026 23:13:45 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 27 Jan 2026 23:13:45 GMT
USER jetty
# Tue, 27 Jan 2026 23:13:45 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 27 Jan 2026 23:13:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Jan 2026 23:13:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4d0d315376e1ff31d7d63f3c3d4b9c25ae75c2615beb89a1ceddddb649c2b5`  
		Last Modified: Tue, 27 Jan 2026 22:13:47 GMT  
		Size: 165.6 MB (165556559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a0344caafcf57f14d91cef00033d1a7a757b669e2e2d58fb1491d610e70641`  
		Last Modified: Tue, 27 Jan 2026 23:13:57 GMT  
		Size: 52.0 MB (52049845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cc1c6d965a2dc690d3ba452e49d98269ef762890c1a4ff5bc1262693d5dfe7`  
		Last Modified: Tue, 27 Jan 2026 23:13:56 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:db915f7688728dbe41edd1d135ae23cb280e62b02cbbc636123796ecf80801ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6171131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729e3f1b15453c0a4791388ba2c136ba76e5e56f7bd91e76278a2a02cecbfc3e`

```dockerfile
```

-	Layers:
	-	`sha256:cf4a6fdff79ee3c9ee40df3a80306b9ceb2f010f22450932df34b6fcf8717c07`  
		Last Modified: Tue, 27 Jan 2026 23:13:56 GMT  
		Size: 6.2 MB (6152812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1beee77d930e639603432fb4ce3460bd55897b7a565dddf3fe252eabce7217ee`  
		Last Modified: Tue, 27 Jan 2026 23:13:56 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d5e823a48f771233084f3460598a9a13346aa99ee676c719d29e081e21d70901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280488476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddd6515056abedafe4f148361f8c3462ce6dc45dc0218fba34900acde699673`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:30:00 GMT
ARG version=21.0.10.7-1
# Wed, 28 Jan 2026 04:30:00 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:30:00 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:30:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 05:39:25 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 05:39:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 05:39:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 05:39:25 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 05:39:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 05:39:25 GMT
USER jetty
# Wed, 28 Jan 2026 05:39:25 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 05:39:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 05:39:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef463fea7a93137770bb91fa14775d030ebc14a22312021b37329181cca2bdc`  
		Last Modified: Wed, 28 Jan 2026 04:30:23 GMT  
		Size: 163.6 MB (163610457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e33989bf486f71f40b09f80c00150707312424cfd4b5900e2c924581f60f3a`  
		Last Modified: Wed, 28 Jan 2026 05:39:39 GMT  
		Size: 52.1 MB (52077253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa56e11a7f87b1d9ee26bf001a92591acc1884ba1f692546b13cb8449f4b0b8`  
		Last Modified: Wed, 28 Jan 2026 05:39:38 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:183ec0c7869dbc5c92f93cc21a8ce2240b960d1109d477768118c73b03487d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54602463ed6c68454661af98424e4c4fdd09d79b3bc314d33b66e1fcf4a94995`

```dockerfile
```

-	Layers:
	-	`sha256:21e6c0895805677f3f371881b1850efa813b0e24e16e1a3bc892cd55492eff3d`  
		Last Modified: Wed, 28 Jan 2026 05:39:38 GMT  
		Size: 6.2 MB (6151477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39792446ec22dc68742496c1dd28e4c3dc6358891367993ea1bc45cc5f423d3f`  
		Last Modified: Wed, 28 Jan 2026 05:39:37 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json
