## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:a2495997d8452cf10d16f9d9f7407944f04a66bde9e70a817640a3539840fb42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:0ba7120278c24f5a799ddf6bc79abe3253934ca620eb47357029d97415abfb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322289923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d108d75c7f5a160e4f903730dc86045a0e052b6028a8184ca13b8c5b56b61b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:24 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:24 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:24 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:24 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 10 Feb 2026 19:08:06 GMT
ENV JETTY_VERSION=12.1.6
# Tue, 10 Feb 2026 19:08:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Feb 2026 19:08:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Feb 2026 19:08:06 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Feb 2026 19:08:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 19:08:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Tue, 10 Feb 2026 19:08:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Feb 2026 19:08:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Feb 2026 19:08:06 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Feb 2026 19:08:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Feb 2026 19:08:06 GMT
USER jetty
# Tue, 10 Feb 2026 19:08:06 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Feb 2026 19:08:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Feb 2026 19:08:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b81996e3b0e5e4ba9a4cc5fbc9979cd889a255b08bc1d9d4e0dc355bca0f3`  
		Last Modified: Tue, 10 Feb 2026 18:32:49 GMT  
		Size: 189.2 MB (189187292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa980d7fb04283d3cfa8d672dc528bc4d0cc22e887bbaf4ef16d12f23e3adea`  
		Last Modified: Tue, 10 Feb 2026 19:08:23 GMT  
		Size: 79.1 MB (79062527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8030a53bfac7c4ae78cedd5d5e1918b3c29c8460c32397c97cdc9ec50c368baa`  
		Last Modified: Tue, 10 Feb 2026 19:08:20 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:77c7ef38a350ea81fc4d0e5894f628f72446f2c06d50addf9d23676f2dd4f737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aedb00114005081d32bf248a9c2b291c898732721dea6228cf8b7a28f024fcc`

```dockerfile
```

-	Layers:
	-	`sha256:5ea0ea74efcd66da9e3d5073bc7bbef5ccbfdb5c3870e16de32a8ad07adf26ee`  
		Last Modified: Tue, 10 Feb 2026 19:08:20 GMT  
		Size: 7.5 MB (7474501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4485641fafc6b7f4758dc8d046a0020bd0ea429bae960025986971cbc32835`  
		Last Modified: Tue, 10 Feb 2026 19:08:20 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d196fe1c1052f3e96694214783dfc7e685a0ed1c7bb1ce2892db3e43ea5c84be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319014048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910ef4451ae27d2bc1fb5e3fa54e0a4e4e0819e306bd81dfb9878223541f4417`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:12 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:12 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:12 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:12 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 10 Feb 2026 19:11:07 GMT
ENV JETTY_VERSION=12.1.6
# Tue, 10 Feb 2026 19:11:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Feb 2026 19:11:07 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Feb 2026 19:11:07 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Feb 2026 19:11:07 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 19:11:07 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.6/jetty-home-12.1.6.tar.gz
# Tue, 10 Feb 2026 19:11:07 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Feb 2026 19:11:07 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Feb 2026 19:11:07 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Feb 2026 19:11:07 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Feb 2026 19:11:07 GMT
USER jetty
# Tue, 10 Feb 2026 19:11:07 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Feb 2026 19:11:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Feb 2026 19:11:07 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098ac51664cc3ecb50ec7d80c5020cda656bac5f9d79fc5f5a1093c71586c098`  
		Last Modified: Tue, 10 Feb 2026 18:32:37 GMT  
		Size: 187.1 MB (187088942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322bc752f09843429e89e355b530336c916a115486c4478ec5e0c711b795c9cb`  
		Last Modified: Tue, 10 Feb 2026 19:11:27 GMT  
		Size: 79.0 MB (79005019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0b6f826c129eb47beaeb21d76e8c3a4947e02a9da08afd7e4e4adc0f32a778`  
		Last Modified: Tue, 10 Feb 2026 19:11:25 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:24aa8e44ab937a5b5b170f57afc0f17553a50957f829eff36ba059677a756a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f7a0657e7464d9de2d51b5739aabe2129546f8c949e89a07e1b6a95a40ab24`

```dockerfile
```

-	Layers:
	-	`sha256:a4ea5024e2940d129234a998e54c7ec0d3963f209a5ab8acf3c24b670d22418e`  
		Last Modified: Tue, 10 Feb 2026 19:11:25 GMT  
		Size: 7.5 MB (7473481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbaca3ebca081045f6da543132ca24b3cdaf4f2da502e64ce5977a2870aae30e`  
		Last Modified: Tue, 10 Feb 2026 19:11:25 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json
