## `jetty:jdk16`

```console
$ docker pull jetty@sha256:e8b0525c9e2ca4cf96b5d8ff6fc9b4be0d60fe85b3a46484340c05e86ebccb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:jdk16` - linux; amd64

```console
$ docker pull jetty@sha256:359f06940cd0a5fbbcf8c3ef5ed3eaf220c609b1da672988dd5585853b6be16c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250191857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0133201d9d213a20c744ae24c8d4c8c3867cc747e5e394b16da1b84f3f8aa3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 12 Aug 2021 19:20:55 GMT
ADD file:ab982d6f37710c434f7ef9650c722d3c6333906cbb9344bf91e79068088bcc69 in / 
# Thu, 12 Aug 2021 19:20:56 GMT
CMD ["/bin/bash"]
# Thu, 12 Aug 2021 19:37:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 12 Aug 2021 19:38:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Thu, 12 Aug 2021 19:38:51 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Aug 2021 19:38:51 GMT
ENV LANG=C.UTF-8
# Thu, 12 Aug 2021 19:38:51 GMT
ENV JAVA_VERSION=16.0.2
# Thu, 12 Aug 2021 19:39:01 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='6c714ded7d881ca54970ec949e283f43d673a142fda1de79b646ddd619da9c0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ffb9c7748334945d9056b3324de3f797d906fce4dad86beea955153aa1e28fe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 12 Aug 2021 19:39:02 GMT
CMD ["jshell"]
# Thu, 12 Aug 2021 20:05:07 GMT
ENV JETTY_VERSION=9.4.43.v20210629
# Thu, 12 Aug 2021 20:05:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 12 Aug 2021 20:05:07 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 12 Aug 2021 20:05:07 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 12 Aug 2021 20:05:07 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Aug 2021 20:05:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.43.v20210629/jetty-home-9.4.43.v20210629.tar.gz
# Thu, 12 Aug 2021 20:05:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 12 Aug 2021 20:05:15 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 12 Aug 2021 20:05:15 GMT
WORKDIR /var/lib/jetty
# Thu, 12 Aug 2021 20:05:15 GMT
COPY multi:aa77a0f6aef2add1a97bf742e5d8ca9322cda3f66ea7673ea49c33da7e5b0889 in / 
# Thu, 12 Aug 2021 20:05:15 GMT
USER jetty
# Thu, 12 Aug 2021 20:05:15 GMT
EXPOSE 8080
# Thu, 12 Aug 2021 20:05:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Aug 2021 20:05:16 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c67289558ae5eb060942db5bf46d182448587a87e21c680a0486b147d4b9a0b4`  
		Last Modified: Thu, 12 Aug 2021 19:22:09 GMT  
		Size: 42.2 MB (42158041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12787f1f3888c64bfc9e779a9705ecc45ae1a60b3757074b6f16cf1d8553cac8`  
		Last Modified: Thu, 12 Aug 2021 19:43:29 GMT  
		Size: 13.4 MB (13373335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bd18e93178b3f1f6de8509b634da7edc7b3c3f556919bc74ebf9cf26011d43`  
		Last Modified: Thu, 12 Aug 2021 19:45:13 GMT  
		Size: 184.8 MB (184807071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f4b89617f55aa177023a4af89615f954efbd45d84af54005e682b07a650daf`  
		Last Modified: Thu, 12 Aug 2021 20:07:06 GMT  
		Size: 9.9 MB (9851961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2936885a60136564c1831f496c5e66d274b41c98e9f706d79cfbfea181ff6531`  
		Last Modified: Thu, 12 Aug 2021 20:07:05 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
