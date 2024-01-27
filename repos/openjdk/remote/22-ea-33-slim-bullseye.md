## `openjdk:22-ea-33-slim-bullseye`

```console
$ docker pull openjdk@sha256:20c25d45bd87f500ea7d98fc416d69826a2365d265e2cc8ed1388d591b3d6ce1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-33-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a88b07f7c4b3a920ce314febd8e53317adf749da16bc633a883e7a0baf957d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235724558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893da0aaddfe042182bd29446becdf5bcf9a4be93a4471a757bbe003ef20d2e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
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
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4104cf6e5533fc573fd4c4d001b8a5cf1f4bca8d4d9e8c429b5da05472c1692a`  
		Last Modified: Fri, 26 Jan 2024 23:50:16 GMT  
		Size: 1.4 MB (1378064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d11f8b462af1538d458aca1d22bd97f51d46eab655bd1ee6e063ae9d6ef2e8`  
		Last Modified: Fri, 26 Jan 2024 23:50:22 GMT  
		Size: 202.9 MB (202928539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-33-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:612ad292c19e6ad6ac573ff67af897cc319f696ec2bbf04b239774795d10d559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9798e4c85d80b45ed4c5d503530dd4b3088dc774667638a0f9361d6e660da931`

```dockerfile
```

-	Layers:
	-	`sha256:dd427a8e11415964cd3488a1268a40a51b973ea223ca3513fca03eee5323c396`  
		Last Modified: Fri, 26 Jan 2024 23:50:17 GMT  
		Size: 2.2 MB (2190189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38abec476d1c48f94044c0241951d1c08f551f3cbfea35202172830f82eca67c`  
		Last Modified: Fri, 26 Jan 2024 23:50:16 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-33-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f76b21dafbedf1cff1af544ed70dcdf7d0998861373f8df0481237cbeccc1100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232408921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7af7776992715e2fccf0c5a79d21e3612c5aa638c49d3e9c794e00c76d496b8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
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
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a4c4865eb908d45fd1c9dfb4d1c3df47f4ed326cf80777309c28a84a352a9`  
		Last Modified: Sat, 27 Jan 2024 20:37:55 GMT  
		Size: 1.4 MB (1361925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e946a14000b7b8b0b6fa300551230dd18cfc36ebd84e98903c8e2022567de1f`  
		Last Modified: Sat, 27 Jan 2024 21:18:15 GMT  
		Size: 201.0 MB (200982986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-33-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ee5e5d86063c009d42e14c2e3f3bc7becd533bea089974933b141a6f7133713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586368b04c360bbe6774d6595fddf5cad34b791e701c71159b574dc959a0b14b`

```dockerfile
```

-	Layers:
	-	`sha256:f96a041822c1aa584e14ab665f70caecbc80aa8a28ee04f0fd22694a1ac5e7e0`  
		Last Modified: Sat, 27 Jan 2024 21:18:11 GMT  
		Size: 2.2 MB (2189547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270bdafb854d568df9cbbbf33f686baf0befa514d4949e552402d04b2014702e`  
		Last Modified: Sat, 27 Jan 2024 21:18:11 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json
