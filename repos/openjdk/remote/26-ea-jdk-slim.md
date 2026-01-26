## `openjdk:26-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:f08c051ec4c1e2725dfc8b44342f3177a02d7c40f84d12579b468211c01c43c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:13929492cb8a6d974eb39a6b0c26f861d27ff2b65412e2b89df0ae71bc32bc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260156033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cd0f5cf34f0ecc76dac884421f7fe732f4933ffe38c362e638cdcc918010a2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:46:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 20 Jan 2026 18:46:52 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:46:52 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:46:52 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:46:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:46:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bda8ee697b8dbbfe2f91e296446db78c346a2d1e7603e894d0ce5a0c377404`  
		Last Modified: Tue, 20 Jan 2026 18:47:11 GMT  
		Size: 2.4 MB (2371073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3b56e0c2ccbea56b035610893a6dabe0c566a0a85fbfa68329191b1896bd11`  
		Last Modified: Tue, 20 Jan 2026 18:47:16 GMT  
		Size: 228.0 MB (228011275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:9b11d04bfd6d6de08e3a8bf06be4fe6d81feb0829660da8ed3ee012d97e81410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff7de7f29817cbfb0c51e7ab1601aeed4d9c6f54e4f69a933d1158a90243df`

```dockerfile
```

-	Layers:
	-	`sha256:4f25d35bca60a9358a285c57e6789ddfa6039b6039bdd4352185b7a22a6554c9`  
		Last Modified: Tue, 20 Jan 2026 18:47:11 GMT  
		Size: 2.3 MB (2278851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7293a2188e078f512b99f5833fb57c983eb35a0ba7795c3ba0e341c93852a928`  
		Last Modified: Tue, 20 Jan 2026 18:47:11 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim` - linux; arm64 variant v8

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

### `openjdk:26-ea-jdk-slim` - unknown; unknown

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
