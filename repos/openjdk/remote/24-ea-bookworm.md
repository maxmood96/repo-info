## `openjdk:24-ea-bookworm`

```console
$ docker pull openjdk@sha256:b47bf2d483926cba7eff8f50aebb65a9957b4d8bb8cb540bbd9cb61e3f306ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:461289d8bbaaaf6eb7bd08e79f5c92525375bb1a14bda887873c02439a251ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366660892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb416d00a4bd84552b97022109c949933963d6fabd4941592f2caa5580f7087c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Aug 2024 18:48:14 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 29 Aug 2024 18:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6ff78227fb6865113ff0e844c0e3dbbd3c3fee0fd03b4a3b3f7134390f785bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='21518bb62faf883eff4bfb1e2c69a5b50d6b3e96b30b0a111f1d1f41a4205fae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88be69a04dd7031427a1614df8e20402c02c12e816f53ef2fc3ac1f0c2e5be`  
		Last Modified: Thu, 05 Sep 2024 00:16:47 GMT  
		Size: 16.9 MB (16943127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b79b1cf36dbc61bcbffa19a2dfc4d790e49ca53824528617ebdc1c4edb2b91`  
		Last Modified: Thu, 05 Sep 2024 00:16:52 GMT  
		Size: 212.0 MB (211959892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:10d18f1607eae20e855768d420e1f83ffc9983b7b8a11cbdb66eea48e72b0dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8275842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f16ab71e710cf12fd7fc01cd3ececc00ac353b495dc13f326206c368fe2d576`

```dockerfile
```

-	Layers:
	-	`sha256:944857d057351f3638ae1a62e4332cb3019b128b1504e860e9f87b794117f5cd`  
		Last Modified: Thu, 05 Sep 2024 00:16:47 GMT  
		Size: 8.3 MB (8257379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830adb59aeb45394a0c8108210648d10d36fb74cc3509e3bd99c53992bb452f3`  
		Last Modified: Thu, 05 Sep 2024 00:16:46 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7ff05872cff20c141152414964ccd9e5cb40a5a92f62df0e578a89de438ae8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364709845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad081db69919f829c4b4ff0c7ca0e5d5a1ff43c1c8d1cf75d7a7c169cd81a5c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Aug 2024 18:48:14 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 29 Aug 2024 18:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6ff78227fb6865113ff0e844c0e3dbbd3c3fee0fd03b4a3b3f7134390f785bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='21518bb62faf883eff4bfb1e2c69a5b50d6b3e96b30b0a111f1d1f41a4205fae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9abf6f7aeed04252d2334ddb555665db4908dc6e1eccb0efd47b3a80b410f3`  
		Last Modified: Thu, 05 Sep 2024 12:57:35 GMT  
		Size: 17.7 MB (17727088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a726d4ba15f81423dba3f3d9657e24ef94a923710507bc74649a94a8051b73`  
		Last Modified: Thu, 05 Sep 2024 12:57:39 GMT  
		Size: 209.8 MB (209805388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9672130a69951da01970f3bf59f432db7a8fe67d89394231dc565df4c08ed35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8413843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c3d4ebe08d498f190672efd9a4d0527294644ac1f4ce7961383b0448e19065`

```dockerfile
```

-	Layers:
	-	`sha256:48e26cba329085d0c5887f7114116d77308e021fa5da3aa60ba39ac2e289d9b8`  
		Last Modified: Thu, 05 Sep 2024 12:57:35 GMT  
		Size: 8.4 MB (8395040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e69e53ed6624b1a35b24aae056930b1beed80fba257dd47755d5a30ce5b709`  
		Last Modified: Thu, 05 Sep 2024 12:57:34 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
