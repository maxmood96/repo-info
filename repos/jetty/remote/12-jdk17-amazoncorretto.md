## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:2acbec74bdc159a3b055c24536f05a8286d264e0b065641dc65b66de3071dee2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4f7c0611290bda3292eba5080b707b932e01888dde6578902f080a7fcdb7e868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267307999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2782b06a492245e675a75c45a99114cc3233142c2f9f6ed9ca6989094e71a08a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 00:19:17 GMT
ARG version=17.0.17.10-1
# Thu, 09 Oct 2025 00:19:17 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:2ed5eb262f0b7dfe71c1c0fc62fc5d0f8b4f6b25e17d18c45cdecf03ed463633`  
		Last Modified: Wed, 22 Oct 2025 00:50:00 GMT  
		Size: 152.4 MB (152417421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792712ff51e39c7bbac38f762b6c3df21183905458f802e8ff80eb79dc0383`  
		Last Modified: Wed, 22 Oct 2025 02:40:24 GMT  
		Size: 51.9 MB (51948082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62fbef6c0e1a64d200f05b9323a793c817e18de69bef28adf6a809be31fee4`  
		Last Modified: Wed, 22 Oct 2025 02:40:19 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:4f02a7928c3abcd8df0ae0ca0b79d368bca680631c059788561810b0f0b16132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fa4b9afad9aab21d05d87178e8c957d43f41224588c9b94fc41f0f2c9f620f`

```dockerfile
```

-	Layers:
	-	`sha256:f31f3b477f13e6e7cd604de877a8b4bba4acd1358217ad21bd332b9c20f70eb3`  
		Last Modified: Wed, 22 Oct 2025 05:18:25 GMT  
		Size: 6.2 MB (6151967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51a1b8ba197f21c6bf180c85815c941db3b7ae867d4d257234dc41b4fb45000`  
		Last Modified: Wed, 22 Oct 2025 05:18:25 GMT  
		Size: 17.4 KB (17396 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:367fb95350c1d7edaabc5b13e827c4a89711af691129ed9f3470026128353c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267787683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd720ce100c83f9a9330b9f3600237b11bb3678f4aa237c52e5c506fadc7866e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 00:19:17 GMT
ARG version=17.0.17.10-1
# Thu, 09 Oct 2025 00:19:17 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:4fd285a6ccc0f7574660524adabe694c5ee580549dd27eb3a1add6f7d397deb5`  
		Last Modified: Tue, 21 Oct 2025 22:13:33 GMT  
		Size: 151.0 MB (150987939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489ec1938b4ad0f9b301aab13c7f1347fc3bb86eab76543cede8cd3587ef1df`  
		Last Modified: Tue, 21 Oct 2025 22:14:33 GMT  
		Size: 52.0 MB (52004660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f329853540ebd9cf6a1a0b1f6ac05d31f9e2c8a11884bc9b66077dccd247617`  
		Last Modified: Tue, 21 Oct 2025 22:14:28 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:d4accf340ad7747f93cb5917408cb46e96d551e959746cf8e03b097b37fba886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee7eee12cf5f827dddafb84ccfa6c7e090e75a20faa2d8575c2c9a812707d8d`

```dockerfile
```

-	Layers:
	-	`sha256:234e2aacc0d1ea516f3b715534bf1f84e19125379ba37578226e4924d20c156a`  
		Last Modified: Tue, 21 Oct 2025 23:18:05 GMT  
		Size: 6.2 MB (6150596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e84dc24548cdd424099e82a9d1a287223cf143bef23957ea98d13ebcb491da`  
		Last Modified: Tue, 21 Oct 2025 23:18:06 GMT  
		Size: 17.5 KB (17488 bytes)  
		MIME: application/vnd.in-toto+json
