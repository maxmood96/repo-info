## `openjdk:24-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:6d113acbc263652bfb8eeffe0ad7359a69442efb2c714b0ad0179acd77f78c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3755af9f95f033aa73828cd7b61f8c75e320b88e0659c8a6926661239585a69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245015499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab067554d0e69cd0014a306c6df7a63b69ded0c7d09681ab0685cbbeaed7738`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Aug 2024 18:48:14 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 29 Aug 2024 18:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6ff78227fb6865113ff0e844c0e3dbbd3c3fee0fd03b4a3b3f7134390f785bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='21518bb62faf883eff4bfb1e2c69a5b50d6b3e96b30b0a111f1d1f41a4205fae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d468ba5404897e81269667302cf4cefc3baa32d1c0b00b8467a66e95ce11d6`  
		Last Modified: Wed, 04 Sep 2024 23:11:31 GMT  
		Size: 1.6 MB (1581809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac85c3f022fc4a2a5945e7c1bacbcb79561e7b30dfa79b6740be247f087d4bd`  
		Last Modified: Wed, 04 Sep 2024 23:11:34 GMT  
		Size: 212.0 MB (212005013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e737fb0c869b336a44809520de5fb2219dc555009e3a0dd2d6b6749dc3539401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2676532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1689aa201a4df31d07ec4ab8e8af0c7e636f4c17876b3b3a5fc0f63e1d0a417e`

```dockerfile
```

-	Layers:
	-	`sha256:ccaba644064041d2921ee03247b8315ded5026ec4e1391c3e9cd30e8d6001efc`  
		Last Modified: Wed, 04 Sep 2024 23:11:31 GMT  
		Size: 2.7 MB (2659174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c396c2444651bc2706f0d7982e7ebd5bb1ace5c8c8f3c990501c692d51a143d6`  
		Last Modified: Wed, 04 Sep 2024 23:11:30 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:017b24c460a889e9fffe4210661b68e849ec544b4315f60f3cf582acf8d1a325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241489575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fa7cebf066a5e428adc9862e9142b3b5ac936225e40a6e1782ac7b39b04f2f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Aug 2024 18:48:14 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 29 Aug 2024 18:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6ff78227fb6865113ff0e844c0e3dbbd3c3fee0fd03b4a3b3f7134390f785bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='21518bb62faf883eff4bfb1e2c69a5b50d6b3e96b30b0a111f1d1f41a4205fae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a37837d4837e78859d09e01c51430b6b2685cea6e27d41e4af3c075e3df4d5`  
		Last Modified: Thu, 05 Sep 2024 13:00:47 GMT  
		Size: 1.6 MB (1565927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbc269763d889e60361ec58b6c8981742dff64d676132a6e3ab1b894853b819`  
		Last Modified: Thu, 05 Sep 2024 13:00:52 GMT  
		Size: 209.8 MB (209849283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:00825440b506f4750bff837b90abb16d2ed3204dd38e2f557b086c6322883287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3810c65a438c14bf7755c4e0b937fc2dc46d7104ba3c477f5859548c06e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:89623167cdd120229af5a1baaa7b71dee06c1ce0816720017782e69d1a56963a`  
		Last Modified: Thu, 05 Sep 2024 13:00:47 GMT  
		Size: 2.7 MB (2659450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a5e190862c67d330118df3f84cd6881ce37038eb6ea283c497d2504d0bd3cd5`  
		Last Modified: Thu, 05 Sep 2024 13:00:47 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
