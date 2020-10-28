## `jetty:jdk14`

```console
$ docker pull jetty@sha256:b80a9372fa57ba9868d1c6e9fcd0ec8525b8ab49bac595c3b8172d5081c78a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:jdk14` - linux; amd64

```console
$ docker pull jetty@sha256:4dd3dec3a62b6b9bf638a47ab50821623695780bc146e8f1592bc2f129062d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.5 MB (276515391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d54a31880040bb88d7b1469000ae65fec31a0a7353b3be7288433f811dcd05`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Thu, 22 Oct 2020 02:16:12 GMT
ADD file:dab686af43f04bdaabbdbe7703e0c2dc85868a5dbb38942747055a44e038f37f in / 
# Thu, 22 Oct 2020 02:16:12 GMT
CMD ["/bin/bash"]
# Thu, 22 Oct 2020 02:34:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 22 Oct 2020 02:34:47 GMT
ENV LANG=C.UTF-8
# Thu, 22 Oct 2020 02:39:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Thu, 22 Oct 2020 02:39:23 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 02:39:23 GMT
ENV JAVA_VERSION=14.0.2
# Thu, 22 Oct 2020 02:40:11 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk14.0.2/205943a0976c4ed48cb16f1043c5c647/12/GPL/openjdk-14.0.2_linux-x64_bin.tar.gz; 			downloadSha256=91310200f072045dc6cef2c8c23e7e6387b37c46e9de49623ce0fa461a24623d; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 22 Oct 2020 02:40:11 GMT
CMD ["jshell"]
# Wed, 28 Oct 2020 00:28:35 GMT
ENV JETTY_VERSION=9.4.33.v20201020
# Wed, 28 Oct 2020 00:28:36 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Oct 2020 00:28:36 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Oct 2020 00:28:36 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Oct 2020 00:28:36 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Oct 2020 00:28:36 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.33.v20201020/jetty-home-9.4.33.v20201020.tar.gz
# Wed, 28 Oct 2020 00:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 28 Oct 2020 00:28:39 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			p80.pool.sks-keyservers.net:80 			ipv4.pool.sks-keyservers.net 			pgp.mit.edu ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 28 Oct 2020 00:28:39 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Oct 2020 00:28:40 GMT
COPY multi:aa77a0f6aef2add1a97bf742e5d8ca9322cda3f66ea7673ea49c33da7e5b0889 in / 
# Wed, 28 Oct 2020 00:28:40 GMT
USER jetty
# Wed, 28 Oct 2020 00:28:40 GMT
EXPOSE 8080
# Wed, 28 Oct 2020 00:28:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Oct 2020 00:28:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:fd3d5e431db632e40b1f1d5ed9a34a906447d43146906e56da1f14f07998bc28`  
		Last Modified: Thu, 22 Oct 2020 02:18:09 GMT  
		Size: 54.2 MB (54161024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004722dc5e0b01dbfaadfde989754299882cd0cd89e7da3f08996ffde63d55e`  
		Last Modified: Thu, 22 Oct 2020 02:44:53 GMT  
		Size: 13.5 MB (13493854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274e305bc330d381645e093243fbb49b07c990eae3cb73a3cff87cf17b6a2c7a`  
		Last Modified: Thu, 22 Oct 2020 02:49:26 GMT  
		Size: 199.1 MB (199088112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7f7843c1febb25999f657de294069c41d5d55b778487350c02d2b7376a756e`  
		Last Modified: Wed, 28 Oct 2020 00:32:09 GMT  
		Size: 9.8 MB (9770952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8040dc2601b339cdc8d10ac08f80f4b60e7813a3e88e502e01e2c152d89ed7df`  
		Last Modified: Wed, 28 Oct 2020 00:32:09 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
