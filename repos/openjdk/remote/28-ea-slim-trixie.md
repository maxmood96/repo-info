## `openjdk:28-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:623a5252bc44db9e16dca6ee9ac8c77c66197c563f0d88d44cefeac603d2b3a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:f5c68c3683f22fda40ebbae1b013f675f61fb530cb17716ebc898563857ac09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259738524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549705d13b61195f00b1289c45c3a2393303486faee852c54a05677cf1c022a9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Fri, 26 Jun 2026 17:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:49:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Fri, 26 Jun 2026 17:49:57 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:49:57 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:49:57 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:49:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:49:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b789bfd2cc265c2dac62906fd605c89d0d533f571f4b69776eea2e94e409553`  
		Last Modified: Fri, 26 Jun 2026 17:50:16 GMT  
		Size: 2.4 MB (2371339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05332fa219b64af31d710b13bd5794234f447f052a74fd1e5780ebcdbb5626dd`  
		Last Modified: Fri, 26 Jun 2026 17:50:21 GMT  
		Size: 227.6 MB (227581766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:44d0a130ffdf446540ec6c8f4a48ba81ecd2d9b68b08edff280b95b99bd28283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d91ef7d7f9d7f7d547e4103ecb4bb38323854d834d27b03a358c197735ab011`

```dockerfile
```

-	Layers:
	-	`sha256:187943cd26eee8c89fa7beae7b657f228c8d7964b487a97bc2c3134a4e1a01a6`  
		Last Modified: Fri, 26 Jun 2026 17:50:16 GMT  
		Size: 2.3 MB (2276372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d0bf5baea68c8faabaf4298b94984eca6f1a798384286b7485b0cc3ac1f5d1`  
		Last Modified: Fri, 26 Jun 2026 17:50:15 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:edf151cb5a88b6587380e53779a8ae9250c847086e465dabbbc9f35edbeba6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258086922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10596971099505caf88ad8584f2ab87932600416e64b3d37fb224130982d6d1a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Fri, 26 Jun 2026 17:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:54:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Fri, 26 Jun 2026 17:54:53 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:53 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:53 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:54:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d4c0715061f3200cf8fefc9c435367746111827f8ba2a6ab87529dcff471bd`  
		Last Modified: Fri, 26 Jun 2026 17:55:15 GMT  
		Size: 2.3 MB (2314550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca54a606dd44687cf9cce042d887d03b56287494782972a8a007e5ee3379a4`  
		Last Modified: Fri, 26 Jun 2026 17:55:21 GMT  
		Size: 225.6 MB (225623821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:54a3c6e0867773d2567a8e21a2ca81118f3cba27ca88a1e42d810dabeec2ec06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6b9f3f379489f58a2f07b7593f505f10ac2b43a1fb8a3894ee11200760dc35`

```dockerfile
```

-	Layers:
	-	`sha256:aa16ca9cfad6881d2a3323beacfb098f0953844be354ba848f5d54e8709eab9c`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 2.3 MB (2276050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ef6b02eba1087e60e87af2e867381df625321d18586f180c671aa75f4e46a7`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
