## `openjdk:16-ea-29-jdk-slim`

```console
$ docker pull openjdk@sha256:77d8fa913b70d36167e8c09a0d2c1d7f64d64d3a43048559e1f41105a6bd3622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm64 variant v8

### `openjdk:16-ea-29-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:20755f7fd1a6d72e64c96e1bbf7ffef0f2615d3e733c749b7c58c0c16eb9cb48
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208534663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af709e3652b30830d2a2428f7fcae4b9f29f3165e537e73be6a9db5b77c4a527`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:08:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:08:44 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:08:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Fri, 11 Dec 2020 17:08:46 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 17:08:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 18 Dec 2020 19:46:25 GMT
ENV JAVA_VERSION=16-ea+29
# Fri, 18 Dec 2020 19:47:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/29/GPL/openjdk-16-ea+29_linux-aarch64_bin.tar.gz; 			downloadSha256=2a273d305f8c5ed1eec0cec322ed37660eddd7bcf1b381583e6c6b66fe020eda; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/29/GPL/openjdk-16-ea+29_linux-x64_bin.tar.gz; 			downloadSha256=484b901cea7c2b6fafea3a4215028f12f225c17807d5413a2d52edcd604ef6ec; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 19:47:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c25fa24001824e973532559552e813948d45a27f9f9f5af2c971a342c8be9e6`  
		Last Modified: Fri, 11 Dec 2020 17:15:22 GMT  
		Size: 3.1 MB (3101003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fccdbc841c29022496434a6931ffba3b0e753a49e80a169a782e0be509c0e1`  
		Last Modified: Fri, 11 Dec 2020 17:15:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb02eac79197dad978a647f1cee34dff2810685cd60f45d68dec1e90805027db`  
		Last Modified: Fri, 18 Dec 2020 19:54:16 GMT  
		Size: 179.6 MB (179577258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
