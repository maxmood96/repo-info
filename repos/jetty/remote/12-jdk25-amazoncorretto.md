## `jetty:12-jdk25-amazoncorretto`

```console
$ docker pull jetty@sha256:649bfed65b59e899b717c8abffdbf4c72de98ad75dcd3af9920ab7656843ed2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk25-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:0c824c344fee30a76a254fda41aee8144c49128440d22840f5487b8dddc559be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322197255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4552b6e35973631fdff830ff90309a23d9733070768cb85477e52f7d0eee0ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:13 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:13 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:13 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:13 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 15 Jan 2026 23:11:21 GMT
ENV JETTY_VERSION=12.1.5
# Thu, 15 Jan 2026 23:11:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 15 Jan 2026 23:11:21 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 15 Jan 2026 23:11:21 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 15 Jan 2026 23:11:21 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:11:21 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Thu, 15 Jan 2026 23:11:21 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 15 Jan 2026 23:11:21 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 15 Jan 2026 23:11:22 GMT
WORKDIR /var/lib/jetty
# Thu, 15 Jan 2026 23:11:22 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 15 Jan 2026 23:11:22 GMT
USER jetty
# Thu, 15 Jan 2026 23:11:22 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:11:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:11:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d88fe3c4b256f3e9e43b9cb5ec26a56a3f9a83b14d7daf8a3ab39250d61c86`  
		Last Modified: Thu, 15 Jan 2026 22:52:23 GMT  
		Size: 189.1 MB (189137832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7323923b801981de45a00f172520e39f4f87e0ce204a537fece5040e27aa99`  
		Last Modified: Thu, 15 Jan 2026 23:11:56 GMT  
		Size: 79.0 MB (79036343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a22f4420638e9bad20b397d5439feeb7996b3594aec9fa32f08fc4fae20bcaf`  
		Last Modified: Thu, 15 Jan 2026 23:11:24 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e69c831580d244422f5acc08563824b497a0229defae5600b94703c459efd562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabd3e477bd3a75e419e9278ec5ea34c5075927a67fa90426b558bec109c2269`

```dockerfile
```

-	Layers:
	-	`sha256:629f417b9473986cdf1c089b0f87b12df5bc929d5d7e2a6d2aa16432669f731a`  
		Last Modified: Fri, 16 Jan 2026 00:19:01 GMT  
		Size: 7.5 MB (7473469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e1c2cb45532cb5c1afc40f5f8f7d9423b1953f3a528d69c00637a9857518f6`  
		Last Modified: Fri, 16 Jan 2026 00:19:02 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk25-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:21ff7945ee8ada77cf3cb1490f855cb9a6ce63d35b1bad080703e3c595fcafd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318891166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a9148f5776326e271fe202bf81113d5682c9fa03a56501bfb4b473175e6b79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:27:35 GMT
ARG version=25.0.1.9-1
# Thu, 18 Dec 2025 01:27:35 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:27:35 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:27:35 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:27:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 29 Dec 2025 22:12:51 GMT
ENV JETTY_VERSION=12.1.5
# Mon, 29 Dec 2025 22:12:51 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 29 Dec 2025 22:12:51 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 29 Dec 2025 22:12:51 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 29 Dec 2025 22:12:51 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:12:51 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Mon, 29 Dec 2025 22:12:51 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 29 Dec 2025 22:12:51 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 29 Dec 2025 22:12:51 GMT
WORKDIR /var/lib/jetty
# Mon, 29 Dec 2025 22:12:51 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 29 Dec 2025 22:12:51 GMT
USER jetty
# Mon, 29 Dec 2025 22:12:51 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 29 Dec 2025 22:12:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:51 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612c39deef61a58a025e6feada7d5e61866b65d460e5d2e64f4d258c21076418`  
		Last Modified: Thu, 18 Dec 2025 02:18:45 GMT  
		Size: 187.1 MB (187059395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97b4e0a37713396ff9fe8bd9552e777f9f34fd358eee17cfcbccc940d8b07b3`  
		Last Modified: Mon, 29 Dec 2025 22:13:23 GMT  
		Size: 79.0 MB (78956445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc8433e67ba3140e5c52b032882a2e400fc65fbbc1b493636b0982a27c812`  
		Last Modified: Mon, 29 Dec 2025 22:12:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e7ae78efb496e676756c1c10746b0427ce25a8bfb0ecb7ab26b3b1dc2a608d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c98ec218a6ab6334435bfe1da4e98995d360765af20c9bc0591b273d6a6bec`

```dockerfile
```

-	Layers:
	-	`sha256:c8df29877ef429b80d9df356451abf112aa0942ce9c5dca64f572fb315cbe6a3`  
		Last Modified: Tue, 30 Dec 2025 00:21:05 GMT  
		Size: 7.5 MB (7472409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfc979f7b7069bbf6a3521f96436f64a4af00c9e3ed3c64916ff37c99f61b74d`  
		Last Modified: Tue, 30 Dec 2025 00:21:05 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
