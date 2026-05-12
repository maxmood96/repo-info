## `openjdk:27-ea-21-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:47ba0d3ba27ff1faa13585cc5a9cdedd3b074c40ac622ef40940b6fe84bdb47a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-21-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:87c328aeff52b3b03a1ec06fe3bc15b4b2a0b155367666248514a9751a2d9840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260957184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c4885380023dbe1479aaab0180e796ba8e157b90b12f0f4efd662ea77cda2a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 23:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 11 May 2026 23:50:35 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:50:35 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:50:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:50:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a7c17530176050b597d17d71cce742e153096ed38c8b1a50fa0d780c76a261`  
		Last Modified: Mon, 11 May 2026 23:50:55 GMT  
		Size: 2.4 MB (2371151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54b660713a4ee35a7a3d7f878788328419d996e42c136dae75e5a13409ad904`  
		Last Modified: Mon, 11 May 2026 23:51:00 GMT  
		Size: 228.8 MB (228805807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-21-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:977b6a951da0f21dd03318aafffa7c8ec0d3a539bc57d16d759732483a333d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75aae5e7d485d848810743fca82656f06bf409277523f16cdf0722d05e6ae4c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4eee7652380aec7ec1b8251e85553bd7858a8ce32dd6b3657cc8a4961619dc9`  
		Last Modified: Mon, 11 May 2026 23:50:55 GMT  
		Size: 2.3 MB (2277625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1512176f67bf38a3dfeb32ee9d090f72f654721941bf3a108e19e61f97977e7e`  
		Last Modified: Mon, 11 May 2026 23:50:55 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-21-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5195776bb343eaa3434915c6ef158ad0f3c7759d12f0ac382dbd94c79ed646b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259230213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805ed3925e57674c09850e3f2285cafcf30f4f5193126602e84464b3f2fd06a4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 23:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:51:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 11 May 2026 23:51:32 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:51:32 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:51:32 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:51:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:51:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55e7a791c519d1f7ca889df0b59dd72e12fb8f88e4f9a0163b1156d20c6d9ea`  
		Last Modified: Mon, 11 May 2026 23:51:52 GMT  
		Size: 2.3 MB (2314408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c5ae9bcafc891e8cb6823e13cb67ede8e63837b7d41824a8a642ca09a21f92`  
		Last Modified: Mon, 11 May 2026 23:51:58 GMT  
		Size: 226.8 MB (226772163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-21-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:bc225592d68e83c5b11f782fa9da2e9dc1196091d77a6ccd564f66b051630e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9dcbac894869deda1d7c5353c838904bb51bb03a6d3197dbf30ca66c3e9185`

```dockerfile
```

-	Layers:
	-	`sha256:b223348f7d2935286427c0a49bf719149c8b771cf4f0534f51ece9ed2db0a353`  
		Last Modified: Mon, 11 May 2026 23:51:52 GMT  
		Size: 2.3 MB (2277311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b63829e299c9bb1d8b06eb2dc48fc0d306a0d9ef83058a71a615963a0c382c7`  
		Last Modified: Mon, 11 May 2026 23:51:52 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json
