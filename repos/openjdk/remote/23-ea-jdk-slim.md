## `openjdk:23-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:dbf58f4abf6c55bad4c09ffa9ac8638accee3ce04114f48249460375a9c4282e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:c92607b9c9abd58d8d19b3fe4399ebdfd21171dc1c558cb9ffe05c12c90aa94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244144778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687c661f43a11eaf172066d980e7911149de2f66abee4cf62ecc444924e0dbf2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 29 Mar 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+16
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='9a5d2039ec965c15d80dbc5106c9e2f1c4a80975e18d308b55f0a3d892f24358'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d654c940f0c5b9ed7549f29066599b2caedbaf2ec45f3745ac35e265c288e2d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7692b50a9e472be56c7e70c8235c2f77767a2e0e0b9ee02b2f85bca280379f1`  
		Last Modified: Mon, 01 Apr 2024 23:50:00 GMT  
		Size: 4.0 MB (4014979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651d09e7854178e73f31b532f2bc9106a1162eb365b22b569e59473454b182b`  
		Last Modified: Mon, 01 Apr 2024 23:50:04 GMT  
		Size: 211.0 MB (211005618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:313bb30261999c2a34e973e243298b06fd4652be8c53b70f5a35e9c1ec7a8b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932149f71ba0d2988a2e27f2f46a109c4e3193c12711627e21d93edfa1e4cb27`

```dockerfile
```

-	Layers:
	-	`sha256:44f4d0ea8827dead72b74b8e38c5e98e6b0af6e4e84ddc91c3f651bbc932b340`  
		Last Modified: Mon, 01 Apr 2024 23:50:00 GMT  
		Size: 2.3 MB (2347504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f411af3ab8cd933dd6c1166754d7ccc68623e0b1eb619849a797fff621feeb08`  
		Last Modified: Mon, 01 Apr 2024 23:50:00 GMT  
		Size: 19.3 KB (19343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5a7ba1aa2fbee5c2825df42f23e9a7070a4f0cdc63dbf91f8e02fbc827c91e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233752172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda6a64b5af9fab4bf12fcc0c2a921ceef286bef9a0541a8950535326580fd09`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63bd5c67700cc24a2dc61525fa979c1c1bf6d9931d1c89140c1658dc404a1d`  
		Last Modified: Sat, 16 Mar 2024 15:54:12 GMT  
		Size: 3.8 MB (3820092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f565065528e03f5f2f15ab39269a07ea91558fb64710a4cefd77263af769429a`  
		Last Modified: Mon, 25 Mar 2024 19:57:37 GMT  
		Size: 200.8 MB (200775646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:72b0a43320c65c5868a044a4d6ca891f3785d821ca02ed1c2acfa3d7b9131267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feef2d14023a8dbd286c8f6d4962e3007ef3a4a7607699e5e2d6df50f3acbe84`

```dockerfile
```

-	Layers:
	-	`sha256:4beec161ecf06f51e10bb41ff525fe6fa68c3764ffb8e442fedffcdc40ecac73`  
		Last Modified: Mon, 25 Mar 2024 19:57:33 GMT  
		Size: 2.3 MB (2346772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39ab0c76d575a740db0a665c59022fbde66ec9e354f62f098806b78b9ec7c7c`  
		Last Modified: Mon, 25 Mar 2024 19:57:32 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
