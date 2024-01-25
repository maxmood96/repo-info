## `openjdk:22-ea-32-slim`

```console
$ docker pull openjdk@sha256:9a7230d75decf60626551fb66a251920f41fd8f6b45f5c8d967fb0b14c61c7fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-ea-32-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:673e8f9badab22b2ba248e410c974a45fc0112f9db7cb95a7b39c8cfe212ef88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236077847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21908b65c43e987519a774aaa73366497c788f166eaae7d7ee52d7be83240814`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 23 Jan 2024 19:48:26 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 19:48:26 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_VERSION=22-ea+32
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='7ac0b8815f22c852796fa13b7680e07fa1dc340aa93f5e2bf1c5502337d952d6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='7c565754b2926817c1779683d6b8f1975a94a8731fad35a670ea669a77aea182'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a364c542abb507b378c344b9c39aa1aca29f085e9b31929b01337de2a54a8b4`  
		Last Modified: Wed, 24 Jan 2024 20:50:16 GMT  
		Size: 4.0 MB (4014868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b10525a477eb6782a60785b9027a0a4976ae6b6b702eb41e3e5e45dae3f2b2c`  
		Last Modified: Wed, 24 Jan 2024 20:50:21 GMT  
		Size: 202.9 MB (202937058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-32-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:204bf4e274329f6bc409f8b324d1b32fc82627ea55ffb77724c9fd2bd8d82e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05264c26c1189e5c044c046c96441023f55201de85ff2a3930d21f0ec293ff40`

```dockerfile
```

-	Layers:
	-	`sha256:a77a435d6f74a59b49a39ee503aecd9a85e3c5c1605bc9931ed0c7491db8034d`  
		Last Modified: Wed, 24 Jan 2024 20:50:16 GMT  
		Size: 2.0 MB (2037187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448c84ce1a2e252033a660e78267448eea8978c8e8e07add0fdd3dfb09bd1614`  
		Last Modified: Wed, 24 Jan 2024 20:50:16 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json
