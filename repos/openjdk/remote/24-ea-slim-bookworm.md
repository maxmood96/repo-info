## `openjdk:24-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:a18e6edfb5e35f4e27c044c584167ce5862d39879bcb946f0ac3255df3cf5430
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:4788cfb953065e6dbacfe733c9bb6920c0fe868353ba7e9ebd84ccdb5c514be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245036156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718d04df5e04b5b2f56533eb393211d61c79f50ba18cfa456cde4bb41d30e8f6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606b9e84610e32d8b7f0766b2232548cb04556c655da31f2df50d5b186af1a4`  
		Last Modified: Mon, 29 Jul 2024 16:56:32 GMT  
		Size: 4.0 MB (4016771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c00c9034eb898413022f9ed9f5d93a9b31272fc4c1afe9f04e83c57689edec`  
		Last Modified: Mon, 29 Jul 2024 16:56:37 GMT  
		Size: 211.9 MB (211893098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4f354a3f6623b96d0a67581e3c565f5929e5c50610c1356ccbf70bf6768a93ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d26d0af51568dabeaf0d69ae0cc8b7ac3346bf58c391ac6295026cb3a663a45`

```dockerfile
```

-	Layers:
	-	`sha256:f8d2bcc7811bf1480503170d352d7c3e76bfd285af57778873182eea18a35a7c`  
		Last Modified: Mon, 29 Jul 2024 16:56:32 GMT  
		Size: 2.4 MB (2365294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c97dc242fc30f8c2bd714964b79e04b0b23d86ef7c9a9ceee7c5182a69b2635`  
		Last Modified: Mon, 29 Jul 2024 16:56:32 GMT  
		Size: 19.2 KB (19210 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:81b4fc0a6fa4de0afc6db77d4bb945e3bf5ca089fdd101cda46accbb2214e099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242752502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3006851f6a3a4b29dc920c33b7280ef99c75e50549e8317ca5ca9ee37dc71d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c349375e2e294f7eff4dd86f726854408dbf40098a96b9250ed96a5be15a73f5`  
		Last Modified: Mon, 29 Jul 2024 16:59:58 GMT  
		Size: 3.8 MB (3829955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0caec7e6e82bd91040033b63915ba7f1c04cbb834d033c8a801a28021aee60`  
		Last Modified: Mon, 29 Jul 2024 17:00:04 GMT  
		Size: 209.8 MB (209765976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2040621045289d222f82b3de9275f1947ca349458c81c6b1669ab8ca41ec0047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc107f76ba13831bec6a6de5b6c8ba8e805da7b4b1431386dfe716998cedf7`

```dockerfile
```

-	Layers:
	-	`sha256:8fd4609d44fdd8f981122441defdfdd75d1820829b2a62611f094ee761a26979`  
		Last Modified: Mon, 29 Jul 2024 16:59:58 GMT  
		Size: 2.4 MB (2365648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a725abeb8caa3ca305a3fcac042c6a4f7a38d4c525240b4614dd419c616733`  
		Last Modified: Mon, 29 Jul 2024 16:59:58 GMT  
		Size: 19.6 KB (19618 bytes)  
		MIME: application/vnd.in-toto+json
