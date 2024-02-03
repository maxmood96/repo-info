## `openjdk:22-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:ce96fab3b2670381af537049ec287c6242642a9fa73ca23c44a914a1c8bc71f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:74e9605223bb101d87f4dda0753595ba9469ef9cdead454d6e44b1f7ced7a89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235723663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad7c4157728a27773a6367311114e24cdb3ffb13f07cb4ede618f471b4257c5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 02 Feb 2024 19:48:11 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='170b7192de3e30c796b95d765b12ca457d3f4b05e97bee0bf81709c8b43cd992'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='63460b6a2c4d547d7a8cf4cf86d67a46f5e6a96a62843a787a2aabdbed4df119'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7971113b28ae169b5eb6d1006c8db56bb28aab312f8641c46e1882f52f5bb5a`  
		Last Modified: Fri, 02 Feb 2024 22:53:36 GMT  
		Size: 1.4 MB (1378070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0eecd52eb74ba9c6f33f65579f4809b433ebd89573aa4fb52cee017ff94082`  
		Last Modified: Fri, 02 Feb 2024 22:53:40 GMT  
		Size: 202.9 MB (202927766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2a25eab4cef1a3d89aeb76e00c6ece1267c70b4715c8e027f4b114a0a3eb5715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa2d0e3bfcf9b07b58e129388a424cb7cdedb805e6cf698234255519df23f17`

```dockerfile
```

-	Layers:
	-	`sha256:53af4507bf5382f7a40b40e8f8fc1cd00a96dfb8ad52dd0989e7ab4ea5a833ac`  
		Last Modified: Fri, 02 Feb 2024 22:53:36 GMT  
		Size: 2.2 MB (2190196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c193179946aeedc0a491d9f4234dc2079b442d15add9f885e93578ca19dd37`  
		Last Modified: Fri, 02 Feb 2024 22:53:36 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4f6655e7e03666411c6e7bcf51aee3873862bcea9c7f803bdb4a68642f2ac056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232409240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6f1672b6d351f4d9bb0c04bd5b01b787904f2bdfb2920b1e5ffadd55eaa03c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:48:32 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3bc7f554a0ea1458559926cfeb111c558c33065ef21aaaadc2eb1182f2acd0`  
		Last Modified: Thu, 01 Feb 2024 16:21:04 GMT  
		Size: 1.4 MB (1361927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd382cee79080a31d9b3d527176502868ab813c66e1868441b4f2325dd3194c0`  
		Last Modified: Thu, 01 Feb 2024 16:22:41 GMT  
		Size: 201.0 MB (200982979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:32a4c73dbcc0c9fee3fb30ec5002a19f8389659c1b1b497e753ebf319b138917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdaaf36c08430bf6c3bb92258d68e6f406804063723f4d3b16c37540cd2d5e0`

```dockerfile
```

-	Layers:
	-	`sha256:d399d30131daf5779155c6e448b914842fd7d2401b2de9f0b20aac13ea1e4e87`  
		Last Modified: Thu, 01 Feb 2024 16:22:37 GMT  
		Size: 2.2 MB (2189547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2216be53ca7a7b6d95ff5661217cec0f3623d4de9170c9ae9f5b6bb370d11539`  
		Last Modified: Thu, 01 Feb 2024 16:22:36 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json
