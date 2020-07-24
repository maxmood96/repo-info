## `openjdk:16-ea-7-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:4b34d4bca15328397113585f4803e7889d369a72f59c6f452f773d006ae765ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-7-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:ce3c5fd104a8ef2988b00a7a3fdb6447b7449d84476835388188c28afe25d77b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227209396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24598b80a2a140a16d7996842a1aaa4916544df12cb15f168dbc7b2cedc4b08b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:35:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 22 Jul 2020 22:35:24 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:35:25 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 24 Jul 2020 19:14:28 GMT
ENV JAVA_VERSION=16-ea+7
# Fri, 24 Jul 2020 19:14:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-aarch64_bin.tar.gz; 			downloadSha256=0e2c7dc384e914fa785087a3970b0ab14f983447e55e663fe5a7b507104f9b7c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-x64_bin.tar.gz; 			downloadSha256=e6d7f1485772b4ac0bdd4681af093a63eb1af7590efca05e950df04a25045a78; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 24 Jul 2020 19:14:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a9ff789daa916dd19c5da227f6e7eb98322425d292eaf4db4bcbd7026bbb6e`  
		Last Modified: Wed, 22 Jul 2020 22:44:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4230aeacaa5e7954882bd141ffbcb4b5aa84abe19e5f89846281cbb9cbfeebb9`  
		Last Modified: Fri, 24 Jul 2020 19:19:38 GMT  
		Size: 196.9 MB (196862201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-7-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:35094371201ae38eb5d512234b8a8aaabf2b224d2352754abbc28d6573acf725
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204388717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16de6c3fc0107adf2c75f0db88038c7a64b6db7b721c6547dae9047f3a0d117`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 06:30:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 06:30:47 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 06:30:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 22 Jul 2020 06:30:48 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 06:30:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 24 Jul 2020 19:34:21 GMT
ENV JAVA_VERSION=16-ea+7
# Fri, 24 Jul 2020 19:34:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-aarch64_bin.tar.gz; 			downloadSha256=0e2c7dc384e914fa785087a3970b0ab14f983447e55e663fe5a7b507104f9b7c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-x64_bin.tar.gz; 			downloadSha256=e6d7f1485772b4ac0bdd4681af093a63eb1af7590efca05e950df04a25045a78; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 24 Jul 2020 19:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0f82184c39547ee9fb75a66e5a70b82b99eb630ad28cdd8523b06be0a51773`  
		Last Modified: Wed, 22 Jul 2020 06:38:56 GMT  
		Size: 3.1 MB (3101443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb1555ec2a284876db227969d24397324383a6ed078947211de8b3d55713e8b`  
		Last Modified: Wed, 22 Jul 2020 06:38:56 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb3c693dd4b4f3d2ec0d7111423049e5d2aeab6d66d90c7cd3ac658004f03d6`  
		Last Modified: Fri, 24 Jul 2020 19:40:03 GMT  
		Size: 175.4 MB (175429237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
