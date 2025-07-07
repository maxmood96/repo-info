## `openjdk:25-ea-30-slim`

```console
$ docker pull openjdk@sha256:f25e7786d30b1830b95cae819c2f5bd2026a20fb72affcfd9fd15a8138e38ee3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:25-ea-30-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:d8e566a4f3516e803ede74e1f01083de78e22906cd8f47a0b429b93b3d0c5711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255486327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814c5720e8a3849e8e0e2d844b4593c387a72e7475c409ebe68f8464541e966c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dd7b170b5b5f435f8522db64ed1ca3fb2f85f4183ae4b692d2cbf0a2be2768`  
		Last Modified: Mon, 07 Jul 2025 20:59:50 GMT  
		Size: 4.0 MB (4024160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a8a1561ecb224a5bce30a53b2b64c671363534c88e6b0ed734bcfb59eae02`  
		Last Modified: Mon, 07 Jul 2025 21:26:22 GMT  
		Size: 223.2 MB (223232024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-30-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:5da784dd81fdb1c98378bc741e4936eba1bca51772e63bb54c28db863e796f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ff0478718eaa006b19cc9a31eaea4ffe8aa0e3c4a9bf21dc48bf499ca6a5a9`

```dockerfile
```

-	Layers:
	-	`sha256:433b7a1f5ef1eab5f8eed32f74ca486dad6595af1fe10926567a0c1278eba5f2`  
		Last Modified: Mon, 07 Jul 2025 21:23:51 GMT  
		Size: 2.7 MB (2653335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af99b44e8443e8171c52113f9718a109335717841ef76aac0ec0896de0944c67`  
		Last Modified: Mon, 07 Jul 2025 21:23:52 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json
