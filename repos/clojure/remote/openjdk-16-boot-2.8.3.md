## `clojure:openjdk-16-boot-2.8.3`

```console
$ docker pull clojure@sha256:37f996094d17babb3b765ecdeb9c23b80f4f04e8aae27e8cec076bba19c69d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:9c9ad1fdd0f50dafbd05e217cd26796eccaab5d616ac481d754b237f68eb488e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286491563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76552027ea5c130723dce1fdcbf680bc0c922d6b5cd4cc356ef23a1c4eac4ec2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:59:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 06:59:48 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 06:59:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Thu, 10 Sep 2020 06:59:49 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 06:59:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 11 Sep 2020 22:33:23 GMT
ENV JAVA_VERSION=16-ea+15
# Fri, 11 Sep 2020 22:33:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-aarch64_bin.tar.gz; 			downloadSha256=c0fda06a69e492907fe85d1e151e34747e0fce3a2221a70e5dcffd8df048d1db; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-x64_bin.tar.gz; 			downloadSha256=7e6eccd3ac82ce7c007b30a8cde4d849c61612be5353de130690646814f5b9f9; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Sep 2020 22:33:46 GMT
CMD ["jshell"]
# Fri, 11 Sep 2020 23:26:30 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 11 Sep 2020 23:26:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 11 Sep 2020 23:26:30 GMT
WORKDIR /tmp
# Fri, 11 Sep 2020 23:26:36 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 11 Sep 2020 23:26:36 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 11 Sep 2020 23:26:36 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 11 Sep 2020 23:26:55 GMT
RUN boot
# Fri, 11 Sep 2020 23:26:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75deccc0fc24a81b45ad439760b94185fe98291ebc80e400f523d6013b5cfdac`  
		Last Modified: Thu, 10 Sep 2020 07:09:23 GMT  
		Size: 3.2 MB (3248472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520097a77d189a857435d7f9537392728ee2fb8781d46cb2b6eb5e3035bfe464`  
		Last Modified: Thu, 10 Sep 2020 07:09:22 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27c2d3b7aa56fe81b4d04428677780f30e79b83d073e7086ad1c9e5c946ec50`  
		Last Modified: Fri, 11 Sep 2020 22:39:02 GMT  
		Size: 197.1 MB (197050820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b6089b738b7755543f27c0ad518041e1cc979e420f14944c42f6bfd281fd25`  
		Last Modified: Fri, 11 Sep 2020 23:29:21 GMT  
		Size: 279.7 KB (279660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7178fe3032b20a4599f9f49ddf6d26e9bf9bfed7560ff450372b8aaa494f4525`  
		Last Modified: Fri, 11 Sep 2020 23:29:25 GMT  
		Size: 58.8 MB (58820238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
