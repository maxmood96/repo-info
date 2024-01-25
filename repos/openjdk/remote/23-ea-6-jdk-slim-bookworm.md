## `openjdk:23-ea-6-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:465c196f5b289c16c51517a9c544796416d35c2ea3529fd03318c667ef1fd01a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-6-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b0bed609c90c979f9e43d32b3f2a2b1ab7ff73176a6362bc21282faf49955c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236371862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3debd835c9d8e09ba114183fde18d3da1a298c448f47f5fd8706606ad6a27f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Tue, 23 Jan 2024 20:18:23 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 20:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_VERSION=23-ea+6
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='5163a8a077bfb1cb60e6b4ade06959b0ecba73399a509a5e83f8f9df5cebd140'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa7e954bb29a17c5d0095c4ce94275bfe53383cb8aa7f14894d352e9c00110c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bccb3718b85e3dcf21c9dbed624fdf4370d5983fd1599017f0728c08e8f8a4`  
		Last Modified: Wed, 24 Jan 2024 20:50:06 GMT  
		Size: 4.0 MB (4014822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c384f962edff71eaab64171a32f63915523bda43cfd98c690414b16b1ab09701`  
		Last Modified: Wed, 24 Jan 2024 20:50:10 GMT  
		Size: 203.2 MB (203231119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-6-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d10dc33744474c95ef82029e7e066cfe4bff6b27cb855ff15326f3d47e0c3e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfe8798eee9f1ee99172e61f040996396e7cc98117788189429708db7e59612`

```dockerfile
```

-	Layers:
	-	`sha256:26f289d985c13ad5284e1b9adbbb2c1c70723c6cf4a80a49a1639878c714d8fc`  
		Last Modified: Wed, 24 Jan 2024 20:50:06 GMT  
		Size: 2.0 MB (2037175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21dfb7839bc7ec05f5e9cc6fa5cd61fe7f0c4d79b3b2366be02a0717c9d5a186`  
		Last Modified: Wed, 24 Jan 2024 20:50:06 GMT  
		Size: 19.3 KB (19327 bytes)  
		MIME: application/vnd.in-toto+json
