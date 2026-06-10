## `jetty:12-jdk17-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:e8964b1b145f844a75347d8514f4a2897ca2941a412091828f70f062ab991a47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:bbb7238f301b36d78694340eb617dbf696ed01feb565dfaf77061ac11761ba34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 MB (290577874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbc89bd229735f45937bbe376365f484c6fa456199d56750711e86f08e18b74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:56 GMT
ARG version=17.0.19.10-1
# Tue, 09 Jun 2026 21:11:56 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:11:56 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:11:56 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 09 Jun 2026 22:06:54 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 09 Jun 2026 22:06:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Jun 2026 22:06:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Jun 2026 22:06:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Jun 2026 22:06:54 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 22:06:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 09 Jun 2026 22:06:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Jun 2026 22:06:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Jun 2026 22:06:54 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Jun 2026 22:06:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Jun 2026 22:06:54 GMT
USER jetty
# Tue, 09 Jun 2026 22:06:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Jun 2026 22:06:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Jun 2026 22:06:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a717de6e4793b1ca17e3ed2ed89ee1c5f60a9dd425f7ed49ec6a2161a40f345`  
		Last Modified: Tue, 09 Jun 2026 21:12:17 GMT  
		Size: 157.2 MB (157156669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f0284962478b5e23f2941abb5035b9ce8a64a747582c1c0e52a15b9c9c672c`  
		Last Modified: Tue, 09 Jun 2026 22:07:11 GMT  
		Size: 78.8 MB (78848173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afab4843b7db214308d8fee884355a7b40183f2564c52510a22309a040869410`  
		Last Modified: Tue, 09 Jun 2026 22:07:08 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:bdab75f20526ed5e95e25e62b6b94f95aae8966845357815db339e3be260c623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba433019b0d2ea6f210231d0c689c9a829c4e9ee114058f0eb14a4823f35ef7`

```dockerfile
```

-	Layers:
	-	`sha256:8157aa55ad17edd277ec23709aca6044a2738bcf7067898ed69e70bfbbdd0df5`  
		Last Modified: Tue, 09 Jun 2026 22:07:09 GMT  
		Size: 7.4 MB (7434042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce3343b905f588b3209e3b8120debfd77cc00b4b8d06818021bcd0c38c285ab`  
		Last Modified: Tue, 09 Jun 2026 22:07:08 GMT  
		Size: 17.4 KB (17439 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:03f27271ab349567000d388c919f7d89952f9da5d4e002192d5a2e65daf3f2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288227370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3468cf97cbee4a9778e052bd2410324b5ac91562044e59cf29619f8e37e801`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:39 GMT
ARG version=17.0.19.10-1
# Tue, 09 Jun 2026 21:11:39 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:11:39 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:11:39 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 09 Jun 2026 22:08:30 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 09 Jun 2026 22:08:30 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Jun 2026 22:08:30 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Jun 2026 22:08:30 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Jun 2026 22:08:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 22:08:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 09 Jun 2026 22:08:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Jun 2026 22:08:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Jun 2026 22:08:30 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Jun 2026 22:08:30 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Jun 2026 22:08:30 GMT
USER jetty
# Tue, 09 Jun 2026 22:08:30 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Jun 2026 22:08:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Jun 2026 22:08:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9206cf5f77622798bf199841bdb1f0985a31fb38d008db3d07e3520a4c2ce515`  
		Last Modified: Tue, 09 Jun 2026 21:12:01 GMT  
		Size: 156.0 MB (155987001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8e6e8880fc1a75c6aee271d5cd50075c1473ad264ebde2cbbe6f267853e823`  
		Last Modified: Tue, 09 Jun 2026 22:08:50 GMT  
		Size: 78.8 MB (78780666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f29171f896d61b6d49e9b93014a6b8cef7284446bd44ec8345a9d5b2281ea`  
		Last Modified: Tue, 09 Jun 2026 22:08:48 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8aa4c6f62528ec214bc530a89beef441051e6bdca309e69795d9ce936848e64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f58552017438feff396b3983a53998ee04f52631dd269e7ccef50eb5689e0`

```dockerfile
```

-	Layers:
	-	`sha256:639134c52f91e7c8bca6656e02fef51278fcd85285359c59d939a67e2161db28`  
		Last Modified: Tue, 09 Jun 2026 22:08:48 GMT  
		Size: 7.4 MB (7432973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab32ee0c8aef26ff36c26f4bafaa1d12863c5558ac1d724d73c3b33afb898e7`  
		Last Modified: Tue, 09 Jun 2026 22:08:47 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json
