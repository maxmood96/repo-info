## `openjdk:26-ea-13-slim-trixie`

```console
$ docker pull openjdk@sha256:74b02d883e4ff75400bebe88c2b368fbb08fa37455b811bd968502dd8ae01792
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:26-ea-13-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:03f3c3fd0d883cd2e27ccf3c3ee2bac59a85a5b6aaeea61a75e3419ef93c6ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255491583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01df12462e64848125279d11ce07d606203edb98c9a513e0c327114b61720a1d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba40873faacf0b0ac49f5fe7340ca09fad17c45810b179ac25395036c0fa28`  
		Last Modified: Tue, 02 Sep 2025 17:24:03 GMT  
		Size: 2.4 MB (2371096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f55e688a1a05b817cb13dc79c142831723ef3740ea1d19810777b580bc8e586`  
		Last Modified: Tue, 02 Sep 2025 18:07:33 GMT  
		Size: 223.3 MB (223347202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-13-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d47be9711d2fcc6c0fdeb3b11b07675573105c8b473b0855d0d8b4c21fcfb63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19108c60b3f9619efd6c9053d5eb1359d836778a4a663a37fc984251b8f89479`

```dockerfile
```

-	Layers:
	-	`sha256:a3e0d29bc74a5313007408ae332b1314007a7043a6a31d8f95bc9dcea0116011`  
		Last Modified: Tue, 02 Sep 2025 18:24:17 GMT  
		Size: 2.3 MB (2281656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebccaccfea510538ad6f231942de673e26c84d66b72e418cba775c1bf0b1a523`  
		Last Modified: Tue, 02 Sep 2025 18:24:18 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json
