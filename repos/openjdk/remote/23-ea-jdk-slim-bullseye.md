## `openjdk:23-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:9460f3711c07b92031cb41699a68f230dfa4abaf3ef6bf0347354f6dd3d2c312
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:62869610292526f07f786f5c7e64b9d3c12481679b47866903ca173a33e62947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244245950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2129f57c804965e99bfd26a6039f352cf24c69b15c97be27d5943569bd7db480`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54201b8dbb717c72bc8a3a4b4028e1a129cea0bfd4cd6e8a9bc74ee0b67380e5`  
		Last Modified: Fri, 14 Jun 2024 01:01:19 GMT  
		Size: 1.4 MB (1378065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc2e8ca484c1705a9fb7db0e056e184550092bebaa016e39fd448de7c87abfb`  
		Last Modified: Fri, 14 Jun 2024 01:01:22 GMT  
		Size: 211.4 MB (211433845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:056d6afca5b34a22f2dde327fb776eb9c21cf56661b24051a2096544d9d9085d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029413af3f8707974cd2eae63bd6099005f5631c2bb46341d6e2ad8cac830be7`

```dockerfile
```

-	Layers:
	-	`sha256:6fc4c2b265fa016f117677216fe4f2820516481ba1bd05696bd67b1a3b65c90d`  
		Last Modified: Fri, 14 Jun 2024 01:01:19 GMT  
		Size: 2.6 MB (2638494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a933e60f8cf392be8f8f3de823d172a28abd7f09a96c1ef0283313dbec52a3`  
		Last Modified: Fri, 14 Jun 2024 01:01:18 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4ad8e0605efbad0f2e54000f8e05cb72533d76c52fd175d4b064c1542234992e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240764282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678ab7cd1129a0d2c1b0484faf9cdc51f191a1621c0974a57553ebacdf9de939`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8abb9c6653ca6c247cb904f25b084470905f4d6682db52ade7c408705b3728c`  
		Last Modified: Thu, 13 Jun 2024 19:58:27 GMT  
		Size: 1.4 MB (1361905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59864175d26e0465054e9a98ab0cc4308c106784784187df7149dc2eda837eb`  
		Last Modified: Fri, 14 Jun 2024 04:14:05 GMT  
		Size: 209.3 MB (209315404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4eb992e13b968ba5492650b01e3b46e8101e1a30a30790bc63c860e695f3bbee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f853a09c63be3d8853c3b89eeb9ead67e51557c49f94db7cc6c3fece3be34`

```dockerfile
```

-	Layers:
	-	`sha256:2a0bcc77a44195f90aab35153c54759f933e861a96ebbf73f9826d6e81753f78`  
		Last Modified: Fri, 14 Jun 2024 04:14:01 GMT  
		Size: 2.6 MB (2638770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141ed664850c26ef3061505de54cda6069639f8dec4f67618e118466f3c5877`  
		Last Modified: Fri, 14 Jun 2024 04:14:00 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
