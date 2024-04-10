## `openjdk:23-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:e7b58a7313adad172d8f2adfe135ee55a31de141dd1f5ba9c75e03e4fb77cd8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:e0a9f57bd7dd3b1a1c338755e9e0bb54a2c758e120fd3a99e94d050f96b04201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244018674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177164be36c41a5002e37a689176a9000f34c91dafe86c077e830b74a37a9afc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Apr 2024 18:48:10 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83262eecb2c3bdb609dab430f50b400b43f7b4bef37e2500a7b2f09297a43a0b`  
		Last Modified: Wed, 10 Apr 2024 02:54:21 GMT  
		Size: 1.6 MB (1581842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424262463bdf0d0f335e91a3635c4e7b204554a6196012de8156baf1229da07c`  
		Last Modified: Wed, 10 Apr 2024 02:54:24 GMT  
		Size: 211.0 MB (211009094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:68a40bd763f8d3469eeaa5b8508fa6941c9deae89160f122442cee70bcf515df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74582508bcc18cbbd63217730ef8ce7281e34b7411bfbfd7ff01c55faf0298e9`

```dockerfile
```

-	Layers:
	-	`sha256:9c7ad575c4381cb007534aa23eec732fb5a7aa315c39b01bb34284c38665e8da`  
		Last Modified: Wed, 10 Apr 2024 02:54:21 GMT  
		Size: 2.6 MB (2638334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d9c6e3a199742e5e0eee03148555a1b94073f4202900517ef9fd0542f65d70`  
		Last Modified: Wed, 10 Apr 2024 02:54:21 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9aad137a039148e55f04fd5b07dbb3eaac1c224489e8895df9c73b65d84cfca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240534680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856db31663c8f0af9bdcdb5b09f44c2cabcb52952030d09ed4415bd41ed0f1e8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a999e7ea0713e0f70812c73c3a44d4933028059c0e0e95008ffb99319b0d52`  
		Last Modified: Sat, 16 Mar 2024 15:56:11 GMT  
		Size: 1.6 MB (1565943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1ceab4f3ddcd41c6c155e6a36a8e3a7a255089c2459f5d353abb267e11cb7`  
		Last Modified: Fri, 05 Apr 2024 18:00:34 GMT  
		Size: 208.9 MB (208897621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce838891bd1c871452ad68b0a9501fc0b3651f8709937d1ec4c3e000fdf3d22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbff243f02a3c3e999c1b67ee6ecac7f271edb9f431a35ed2f99b725a0eac40`

```dockerfile
```

-	Layers:
	-	`sha256:9f020256256b12722cf898ef26a2627126e53cc6c48815108d88e9e3b9e6d299`  
		Last Modified: Fri, 05 Apr 2024 18:00:31 GMT  
		Size: 2.6 MB (2637586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c619df0334c2aab1214d4ca973763451c99239a8f366d4b7a2006469165c5d`  
		Last Modified: Fri, 05 Apr 2024 18:00:30 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json
