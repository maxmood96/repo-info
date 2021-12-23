## `jetty:latest`

```console
$ docker pull jetty@sha256:f92dd94888133aec350f4dc37c79e32218d94e221973528775b1841f16cc81a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:latest` - linux; amd64

```console
$ docker pull jetty@sha256:4ec91c819fe38e19a4b5521fab1b62fbf1e4a3779feaffad8040572126814a6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252674573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fd309d204667e6f66056ef8b19f0ff224b41a5ed3d008e7e5697790cf30c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 23 Dec 2021 02:20:57 GMT
ADD file:15b307e0b1aafead42c103e34d3e51a271acea1ab0b68961e239f11af3b0d179 in / 
# Thu, 23 Dec 2021 02:20:57 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:37:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Dec 2021 02:39:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 23 Dec 2021 02:39:05 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 02:39:05 GMT
ENV LANG=C.UTF-8
# Thu, 23 Dec 2021 02:39:05 GMT
ENV JAVA_VERSION=17.0.1
# Thu, 23 Dec 2021 02:39:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Dec 2021 02:39:16 GMT
CMD ["jshell"]
# Thu, 23 Dec 2021 03:26:57 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Thu, 23 Dec 2021 03:26:57 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 23 Dec 2021 03:26:58 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 23 Dec 2021 03:26:58 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 23 Dec 2021 03:26:58 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 03:26:58 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Thu, 23 Dec 2021 03:26:58 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 23 Dec 2021 03:27:04 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 23 Dec 2021 03:27:04 GMT
WORKDIR /var/lib/jetty
# Thu, 23 Dec 2021 03:27:05 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 23 Dec 2021 03:27:05 GMT
USER jetty
# Thu, 23 Dec 2021 03:27:05 GMT
EXPOSE 8080
# Thu, 23 Dec 2021 03:27:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Dec 2021 03:27:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:155aced2666332ddff5a741b0236f360820e7aa3fc3dde2224fc17a91fc48db6`  
		Last Modified: Thu, 23 Dec 2021 02:21:56 GMT  
		Size: 42.1 MB (42105152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5901c58ecb29b61159b5e3a63dfbb0fb520b2de1d33c9fb038d9b697e3fcd4`  
		Last Modified: Thu, 23 Dec 2021 02:45:32 GMT  
		Size: 13.5 MB (13520734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1076e441ffb58eee60f1bab40db6ca69a01e33346eff212eac1191e6b754bd`  
		Last Modified: Thu, 23 Dec 2021 02:47:53 GMT  
		Size: 187.2 MB (187170395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f338dc443b128a2e65ca81f66ad3e95f70f748784e0848c3d115d916fe668a0b`  
		Last Modified: Thu, 23 Dec 2021 03:29:32 GMT  
		Size: 9.9 MB (9876853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9496236305ea8ef69baeea39de56856e7df456fd43e3b7b76dd7829512d682`  
		Last Modified: Thu, 23 Dec 2021 03:29:32 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:latest` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:66e7b19d9379b45d0b20ce4dfe91459796c12644224afb67e9fd401eb51a230a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252177417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d53e5120fb4437bae537d64e6424b479684cbf18b3ed8919d34f8ac54aabf2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 23 Dec 2021 02:40:45 GMT
ADD file:140d632303428d802f77f473aef33fa52daacdfc76b23edde4344be661c1d4b0 in / 
# Thu, 23 Dec 2021 02:40:46 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:58:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Dec 2021 02:59:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 23 Dec 2021 02:59:41 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 02:59:42 GMT
ENV LANG=C.UTF-8
# Thu, 23 Dec 2021 02:59:43 GMT
ENV JAVA_VERSION=17.0.1
# Thu, 23 Dec 2021 02:59:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Dec 2021 02:59:54 GMT
CMD ["jshell"]
# Thu, 23 Dec 2021 03:44:46 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Thu, 23 Dec 2021 03:44:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 23 Dec 2021 03:44:48 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 23 Dec 2021 03:44:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 23 Dec 2021 03:44:50 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 03:44:51 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Thu, 23 Dec 2021 03:44:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 23 Dec 2021 03:44:58 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 23 Dec 2021 03:44:59 GMT
WORKDIR /var/lib/jetty
# Thu, 23 Dec 2021 03:45:01 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 23 Dec 2021 03:45:01 GMT
USER jetty
# Thu, 23 Dec 2021 03:45:02 GMT
EXPOSE 8080
# Thu, 23 Dec 2021 03:45:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Dec 2021 03:45:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:53f096d4aa0757c30613f325df1e03a90db9d9879ea251b394e3ab0a068b5610`  
		Last Modified: Thu, 23 Dec 2021 02:41:44 GMT  
		Size: 42.0 MB (42018351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921862a08fd8bc652539d62804daf06ab6464bd5b42061f5bedbdfa73bd62136`  
		Last Modified: Thu, 23 Dec 2021 03:11:46 GMT  
		Size: 14.3 MB (14303905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5e67fcac32d1d4b20751372e66e4b457cc5644d14505043285d47f485d041`  
		Last Modified: Thu, 23 Dec 2021 03:13:18 GMT  
		Size: 186.0 MB (185976992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02574c504277c8cac456cbdd454d8547d97bff6eb8aae1887f1230ed561654`  
		Last Modified: Thu, 23 Dec 2021 03:49:18 GMT  
		Size: 9.9 MB (9876728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0bfb773c76bce5f4c920d81f3fb9060dd5b8fa72f91302d4b8455e32fd92b6`  
		Last Modified: Thu, 23 Dec 2021 03:49:17 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
