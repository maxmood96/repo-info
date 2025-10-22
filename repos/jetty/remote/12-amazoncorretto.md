## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:494bae2f490f01057d11a576b96861b7524f8be97c392bdaddb5d455897140b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:04af5235dc65cf21d69934e2bf500e7e0beed5bbd74fb06865d418d0aae6b44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280379073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fc53ab0f3c3f738f511d76fe2e5d858fda94821c2ce141af834eeac71d54c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 00:19:17 GMT
ARG version=21.0.9.10-1
# Thu, 09 Oct 2025 00:19:17 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_VERSION=12.1.2
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.2/jetty-home-12.1.2.tar.gz
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 09 Oct 2025 00:19:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
USER jetty
# Thu, 09 Oct 2025 00:19:17 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Oct 2025 00:19:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Oct 2025 00:19:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d592fe075709c62638ad9b0b8b67157100093faaa06408e582bdceb37cb6083`  
		Last Modified: Wed, 22 Oct 2025 00:36:57 GMT  
		Size: 165.5 MB (165487938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b05bc88875ed25296d9e514d39ed940f1015f5f62ebe3201adeb7e259dabc21`  
		Last Modified: Wed, 22 Oct 2025 02:40:26 GMT  
		Size: 51.9 MB (51948639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90fa68283dbfb8bd262333456a2459f21162bceeb85c4b4e29d2a8b3e77218`  
		Last Modified: Wed, 22 Oct 2025 02:40:18 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:64d01617b00d94cc814fb9ed305e5af8840d0e7d602fc9c3ea80ef645881046d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6171192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79fe03a39313a66002cbbc3c7266e82ca78056131d734d50bdc76e3aa2b0830`

```dockerfile
```

-	Layers:
	-	`sha256:c584dcabe8f99c5dd8568edc68b27f1fc5e0b15ced42018e68a129f9d9b2005b`  
		Last Modified: Wed, 22 Oct 2025 05:18:17 GMT  
		Size: 6.2 MB (6152830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588d92d27c400fd403d07fe12fd511bb0caf4af87099b7b05c460b4dcb799a5d`  
		Last Modified: Wed, 22 Oct 2025 05:18:17 GMT  
		Size: 18.4 KB (18362 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2abbf6454b6d5caba03a40708f4669ede69436ba8172c6a051dd319864560acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280387520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdee149503bd9eaea61291a846faa6b6946640f1da5bdc9c3d1fb0b0b671319`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 00:19:17 GMT
ARG version=21.0.9.10-1
# Thu, 09 Oct 2025 00:19:17 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_VERSION=12.1.2
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.2/jetty-home-12.1.2.tar.gz
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 09 Oct 2025 00:19:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
USER jetty
# Thu, 09 Oct 2025 00:19:17 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Oct 2025 00:19:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Oct 2025 00:19:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c99654ecaa79d9c18ade13301c62620d4fd6ffa16a1f4b1d2b9003f55592d`  
		Last Modified: Tue, 21 Oct 2025 22:13:26 GMT  
		Size: 163.6 MB (163587188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed215241a7ac6d2e842aeeec6835a0daa77e1d8738afe923c44eb55fb5a8cf9`  
		Last Modified: Tue, 21 Oct 2025 22:14:20 GMT  
		Size: 52.0 MB (52005248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b8afd471edadeb3ca178c8b330545fdff60683bfb2f5a600596e98dbf3c9f`  
		Last Modified: Tue, 21 Oct 2025 22:14:15 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:70309cf5a0992c52f72c118318699b4246f015b4efe2bcf353bce9a25564ee32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba7548107f79c9023bfa31d36d128bcaf371de17da3b506fed9c3eadd02d460`

```dockerfile
```

-	Layers:
	-	`sha256:4cec7d6316cf18087a79c7c14bc4511a089095bb7d0bcc878d505fcab5e426d4`  
		Last Modified: Tue, 21 Oct 2025 23:17:31 GMT  
		Size: 6.2 MB (6151495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4379447b68e277e5876ec34ff4a9c433613b6c140572bc9ec44047ecb3adc03e`  
		Last Modified: Tue, 21 Oct 2025 23:17:32 GMT  
		Size: 18.5 KB (18490 bytes)  
		MIME: application/vnd.in-toto+json
