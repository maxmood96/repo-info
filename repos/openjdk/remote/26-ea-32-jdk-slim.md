## `openjdk:26-ea-32-jdk-slim`

```console
$ docker pull openjdk@sha256:e2e9ae9fc88218977a4db035a2d53d82fffe07c3105aa114f68bac531547ae97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-32-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fe169857dbdb2b9496c52e64ca8725fa16a44a04b2e47b6c35c2a4f6095a4207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258405431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080d4fdaf0c7444be6667a7d6bb11e02bca115fe8f2cdc805790b2f45c5cffa1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Mon, 26 Jan 2026 22:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:10:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 26 Jan 2026 22:10:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:11 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:10:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35944f1ead688dec5b985b31ccc6b3f55bcd565a580d750b57f5c9f426712d`  
		Last Modified: Mon, 26 Jan 2026 22:10:31 GMT  
		Size: 2.3 MB (2314189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686999ce5f713fa7999908d82b268e8ef17e52b358a14f18d1495926e3fc42b3`  
		Last Modified: Mon, 26 Jan 2026 22:10:36 GMT  
		Size: 226.0 MB (225957200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-32-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef368461f485457ce7b3f2f22c779218a54ce2a5006c0430d0629b7199b42752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13c40409d53757b37ca5f89477dc4d4e843b2e31ee994654379a857581e62b2`

```dockerfile
```

-	Layers:
	-	`sha256:5326f8b8fbd6caa32dd590bf4dc9b02f41b29c02d725577e258a8237abbea44a`  
		Last Modified: Mon, 26 Jan 2026 22:10:31 GMT  
		Size: 2.3 MB (2278537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdda712b49b370e83f1255bea2345ef83c92e24ee41e6c310b66258e1c92913e`  
		Last Modified: Mon, 26 Jan 2026 22:10:31 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
