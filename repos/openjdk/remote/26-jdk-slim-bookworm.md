## `openjdk:26-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:d17e209e05faabbe259800d7071a31efa21fb3fc5e2ead04c07c71cea59275d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:9db840deed84914c5fb00de56371e1a64b55dfe25ec7ea41e2a3261e73363002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258220306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3702f9e2a728fa272983442a2f324ae8c860697efd22562e022b2ceeabbb3410`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 31 Oct 2025 20:29:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:29:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 31 Oct 2025 20:29:54 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:29:54 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:29:54 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:29:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:29:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba59a62650df647a7d53e45445ea933a0ca2b0a168e91b4ff23750fbd1d9f8`  
		Last Modified: Fri, 31 Oct 2025 20:30:27 GMT  
		Size: 4.0 MB (4027336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee19ec0600f4f74856a5989317785ab299a727db5e8db848bca541a82e25a21`  
		Last Modified: Fri, 31 Oct 2025 21:26:04 GMT  
		Size: 226.0 MB (225964649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:62e997f2b3a142778e4829731e36f488bd054627135747d42c6d8eb65abb8f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c2c7e7445ea01381c28f1c4ad8a7d8b158b5b4cb6024b99269d396b18c7b1c`

```dockerfile
```

-	Layers:
	-	`sha256:1ebd1693a7abd9a89b45734e9f2f0beb99c051389e730cb4ac4b0d626942d944`  
		Last Modified: Fri, 31 Oct 2025 21:24:16 GMT  
		Size: 2.7 MB (2651070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51278524f387f9555e061099e37afbc67f86df657142a4aa7db256b77135bac8`  
		Last Modified: Fri, 31 Oct 2025 21:24:17 GMT  
		Size: 17.5 KB (17526 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c58beb05bbba63e19eb7e5023fd2e98f144ab562f3422d470b40ca958a4192f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255771283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585c996c0f91230678a78b887ba2cf5252d23539d08a4efeae952ad74930a7cc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 31 Oct 2025 20:10:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:10:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 31 Oct 2025 20:10:44 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:10:44 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:10:44 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:10:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:10:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ef720c02c38e60413edb338062a88b614892a46c5eba05e226d0eaf8ee4e92`  
		Last Modified: Fri, 31 Oct 2025 20:11:22 GMT  
		Size: 3.9 MB (3851390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bfbfb7d5aed36bb5d937448ca4bf55f89b508faefcffe408919ea5f927463d`  
		Last Modified: Fri, 31 Oct 2025 21:26:52 GMT  
		Size: 223.8 MB (223817703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9c80c757645c4c16bd1feb5b1a664142e80d23dca0f3dae99fe5ffaefed4ea01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b563eda5e8c77bc6f771156aac854a1090a593df5046db5d19a61a134fb0e2b`

```dockerfile
```

-	Layers:
	-	`sha256:8bd0c8a157de2c0172224cfbc0be551ccef692dfcb33d3613b23d208cbd70d51`  
		Last Modified: Fri, 31 Oct 2025 21:24:21 GMT  
		Size: 2.7 MB (2650728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84447125130ad7d96a6ad65c1e5e5bceb3291db7459b34c2e07679ee1d2d2dde`  
		Last Modified: Fri, 31 Oct 2025 21:24:22 GMT  
		Size: 17.7 KB (17670 bytes)  
		MIME: application/vnd.in-toto+json
