## `openjdk:26-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:696c183b31313e30bd35deb62f3b97012190613eee30e9da0b1f0703a58adea1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:91dafec15667e004864b8e43422579e466d8795713b30787997450eef2c6d442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255452688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66c3a74d23dcaf43c7c5e6105f50789d82661cf6e7c03a50a4966d9a2e98e2a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3ba490f6f0181e42e7054f873b1cf7b90eb6dac994c6e733229fc223594c5e`  
		Last Modified: Mon, 18 Aug 2025 21:34:27 GMT  
		Size: 4.0 MB (4027236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09576c8914e47020ae680b7225ec0929096025861e6e0743c44594dd45e4cdcb`  
		Last Modified: Mon, 18 Aug 2025 21:35:15 GMT  
		Size: 223.2 MB (223195197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ff91f919a66a271a7ccb1a9eb12a63b959a9681cef9fa89db26cec1ce6274d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107291674f088b9b7fe4df1c47ce00b79cec9e240542f9d9a2eeae878cd9f9e`

```dockerfile
```

-	Layers:
	-	`sha256:bf878f14c598af23b5296fcc201dece0f26219a83c193f837bc72ef419beae30`  
		Last Modified: Mon, 18 Aug 2025 21:25:17 GMT  
		Size: 2.7 MB (2650833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:001978e33d3f837347bf4c79900fa8d4d5b7e7254e7962e8881d3dcec7e4097a`  
		Last Modified: Mon, 18 Aug 2025 21:25:18 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a784838eefac47056bf7e386177be0ba3bcbd8c860e9e928d38d0a87439db6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252967610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7aa3c1e76980d09223e329ed0634e821ed333033f36ec36e90bf0eab885160`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18619d6149826238e20d8c833bd88d9141048eb6c0b28fbe96d458d21ffae3c4`  
		Last Modified: Mon, 18 Aug 2025 22:25:41 GMT  
		Size: 3.9 MB (3851380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a2690a30b6a69f4df2ec8398f9109b04ded34eb8c7255cc133f190fbdc7811`  
		Last Modified: Mon, 18 Aug 2025 22:25:34 GMT  
		Size: 221.0 MB (221034229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:935d19ac7c3aad7e473571a9d77ce7a58a62321b0b6567424cdb89cc0098f3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96306a117cdc3c889f5bea5351b8aca2ad094396c8191e06faaaf11563730aee`

```dockerfile
```

-	Layers:
	-	`sha256:6eb8fffecae6cd726ddedd58e00627273eb16afcacbb0c189ea01fefecfdc2ff`  
		Last Modified: Tue, 19 Aug 2025 00:24:53 GMT  
		Size: 2.7 MB (2650491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b5830a0721794cb0cdf56d8c535396d7e9ca5f0110acd881948a5d5a88cdd0`  
		Last Modified: Tue, 19 Aug 2025 00:24:54 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
