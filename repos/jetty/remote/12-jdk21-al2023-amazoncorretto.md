## `jetty:12-jdk21-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:c69100157b377fe00a20013bd015bda47483058e6804a36cb1f4223f4e52a01e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:5132c2bd721f67db0655e686fcc5f537b424b61ab6d87ae0a36b8fbd769812bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304238238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe93347006d2511936a8ede8f0557eb3c1f941098ba0401601563da15817dbe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:12 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:05:12 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:12 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:12 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:16:43 GMT
ENV JETTY_VERSION=12.1.10
# Mon, 22 Jun 2026 18:16:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 22 Jun 2026 18:16:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 22 Jun 2026 18:16:43 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 22 Jun 2026 18:16:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 18:16:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Mon, 22 Jun 2026 18:16:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 22 Jun 2026 18:16:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 22 Jun 2026 18:16:43 GMT
WORKDIR /var/lib/jetty
# Mon, 22 Jun 2026 18:16:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 22 Jun 2026 18:16:43 GMT
USER jetty
# Mon, 22 Jun 2026 18:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 18:16:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 18:16:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbda8bbed2402313490b832b371f9a31cefa72cc0c1f79f7de0207d319faaf9`  
		Last Modified: Mon, 22 Jun 2026 18:05:38 GMT  
		Size: 170.4 MB (170446421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0d160002d60bf911c71be8e65f1d449d2da1e4a392b0a98f9f283d34e51875`  
		Last Modified: Mon, 22 Jun 2026 18:17:02 GMT  
		Size: 79.2 MB (79215758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82969b48dc99ce99869b15ec65625ce00911d162529a86ae786a74ca72845d54`  
		Last Modified: Mon, 22 Jun 2026 18:17:00 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e252b3f854289a9f24ea8f29e8ebddd1a8d89bdb13175da36e276478e427fc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f202f44c748756ddd799bcb9568695748942b90336f42e4f28b66aa8e0b38d`

```dockerfile
```

-	Layers:
	-	`sha256:33eb4b3fd9f59122807e43d22be17c99c023832b346de184ef226e3d87091b5d`  
		Last Modified: Mon, 22 Jun 2026 18:17:00 GMT  
		Size: 7.4 MB (7441611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162e8a509e1506f406eb4bd0a0025ffedb5686920714ec122a647cb588bab582`  
		Last Modified: Mon, 22 Jun 2026 18:17:00 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:ec5528edde5038fe906451de5d34e3bbd751db7bda154f8fc921eaf5010f61e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301273221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4934c84f3389fb90ecab779cd3b99d467d1a347681cecf2e8405975a8b1230d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:10 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:15:10 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:10 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:31:25 GMT
ENV JETTY_VERSION=12.1.10
# Mon, 22 Jun 2026 18:31:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 22 Jun 2026 18:31:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 22 Jun 2026 18:31:25 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 22 Jun 2026 18:31:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 18:31:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Mon, 22 Jun 2026 18:31:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 22 Jun 2026 18:31:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 22 Jun 2026 18:31:25 GMT
WORKDIR /var/lib/jetty
# Mon, 22 Jun 2026 18:31:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 22 Jun 2026 18:31:25 GMT
USER jetty
# Mon, 22 Jun 2026 18:31:25 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 18:31:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 18:31:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10beb5c68f4d3c7d1c45314bbff9c0bb6baf58079563b749b2f64ac9f3c511d3`  
		Last Modified: Mon, 22 Jun 2026 18:15:34 GMT  
		Size: 168.7 MB (168721711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0d48109b0738b0d8773627a04d63814ca1c596ea10d847bb9ca9af1d930707`  
		Last Modified: Mon, 22 Jun 2026 18:31:45 GMT  
		Size: 79.1 MB (79098948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5969498491265b77d1386c026f759bcd8c6718728d589b5350d91c05d836cd`  
		Last Modified: Mon, 22 Jun 2026 18:31:42 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c50245a1870e11b1914384f172d6bdb3e917b3b580616ec078c2aa836a435ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7458077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee1eeecc4072110b8d75df541d283cc2466eb978d6c8f2ee5f5ba9b2accd249`

```dockerfile
```

-	Layers:
	-	`sha256:da09334278448bbaa26d670814a6a8a59724268634807a3d4fdb7a6a05dbb63d`  
		Last Modified: Mon, 22 Jun 2026 18:31:43 GMT  
		Size: 7.4 MB (7440545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecb2a39eaa5093118bf94ea63795e2f7fb56b0e92745cf738e98e3f0139befc5`  
		Last Modified: Mon, 22 Jun 2026 18:31:42 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json
