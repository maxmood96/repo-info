## `jetty:12-jdk23-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:273e8122afda0efdb4868b6b0dbf1a6fa96d5e037f5d138d05e50efb6ee5692d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk23-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:89cc6e897e8233b3b9d18bb7028d1e9f9a39b975a0b27de98b2679d2b37beb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298105413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22be6bc24565c9dda5155dac323bcfdcadb9b017d051b582193419a0cd355b6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_VERSION=12.0.17
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.17/jetty-home-12.0.17.tar.gz
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 07 Mar 2025 02:59:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 07 Mar 2025 02:59:45 GMT
WORKDIR /var/lib/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 07 Mar 2025 02:59:45 GMT
USER jetty
# Fri, 07 Mar 2025 02:59:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 07 Mar 2025 02:59:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Mar 2025 02:59:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7af05e057fd5e223e72a7d86db6ccf9a1448d643657ef1e37b69605210c97`  
		Last Modified: Thu, 27 Feb 2025 21:08:47 GMT  
		Size: 177.6 MB (177592724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe7c75940da6154b8fb6a8138921d82f774cc7461e0e307d1549353486f18b9`  
		Last Modified: Fri, 07 Mar 2025 22:08:41 GMT  
		Size: 67.4 MB (67359263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9896df2e9acafacfbe71704ff4dbb10f94e858f2d12fcd34dade53544f17e7bc`  
		Last Modified: Fri, 07 Mar 2025 22:08:39 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk23-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:4c67b64e8ea432b0849fb0a181d1cc158e4e9aafb3874a7042789677f2a9b563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991bd0d024c820d70624945e759c97ffd3ddf65bd4340456c2f626db6310f1b9`

```dockerfile
```

-	Layers:
	-	`sha256:edad6d7d7c10a02ce5cdfa6be73c363fcb49ba8791bbe55b3d18545e80a346a1`  
		Last Modified: Fri, 07 Mar 2025 22:08:40 GMT  
		Size: 7.3 MB (7322244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06dddf6d9187db4b88f5c39d69eca459c20d48517f930d3ca1dfb68947d552fc`  
		Last Modified: Fri, 07 Mar 2025 22:08:39 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk23-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a4bb097913a0f7d8772ded58ca933bf8c4c8951159576a57de79d29ce41aa2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744c480fdc49e53a70cf32f8d556b6d44632067ca93022729d83842d4eb9a391`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_VERSION=12.0.17
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.17/jetty-home-12.0.17.tar.gz
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 07 Mar 2025 02:59:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 07 Mar 2025 02:59:45 GMT
WORKDIR /var/lib/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 07 Mar 2025 02:59:45 GMT
USER jetty
# Fri, 07 Mar 2025 02:59:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 07 Mar 2025 02:59:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Mar 2025 02:59:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54469013ccf794077e3663cbfeb27227feeda108f7a6a129eaac54867444c07b`  
		Last Modified: Thu, 27 Feb 2025 21:24:55 GMT  
		Size: 175.6 MB (175622009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abfdc9b3e2781ca9c90eb3a03e4989a4f8846a3a72bc95745857490be38ccf1`  
		Last Modified: Fri, 07 Mar 2025 22:15:08 GMT  
		Size: 67.4 MB (67407881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c88cb78a4bde118f5bbcb751eb1d6b5eca1689cc8cd3f232d47e4f1ea21adf`  
		Last Modified: Fri, 07 Mar 2025 22:15:06 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk23-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:00417e92c9a4dad861282981ea7d89df096550583ca59e4d5741544a9c2f6d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3613cb1fb4dc4f489c04c15c3a207e2f1601885d09321a7a555334e3c969e3f7`

```dockerfile
```

-	Layers:
	-	`sha256:0ef1587560406aa2a3149ac55ed35b0ee860ddbb4528121f0316757bb7f988b7`  
		Last Modified: Fri, 07 Mar 2025 22:15:07 GMT  
		Size: 7.3 MB (7320364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d7068471cd31b786d5b03fad35e178915bd2b595cc94e18da9f3f98a44b75c`  
		Last Modified: Fri, 07 Mar 2025 22:15:06 GMT  
		Size: 17.6 KB (17575 bytes)  
		MIME: application/vnd.in-toto+json
