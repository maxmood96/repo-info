## `openjdk:25-jdk-bookworm`

```console
$ docker pull openjdk@sha256:795cffee2e7ffc2160cd8bafc5676fa254fe11b4b08a8a009704b313f0b6f4ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:1872a524912451440e8a6e0b6ec5b1f654e182791acf4086ead55cb74f1390a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 MB (377043235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd59a3cac11e6ef36de611317b7b62bb88e731cfbd6b6a0a3efc999ad107f6a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 09 Aug 2025 00:48:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_VERSION=25
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95def226524a16af99dec2a2e54589cb8f61514de3fc4deb72748306c7e2f32`  
		Last Modified: Wed, 13 Aug 2025 01:10:46 GMT  
		Size: 16.9 MB (16943295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db32e2dfb65698e5a469ce925b591c7ccfb6ec86707f92da528071c0f9291064`  
		Last Modified: Wed, 13 Aug 2025 01:10:56 GMT  
		Size: 223.2 MB (223184538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fbef07d324bcc8152a0d09d401812821b7e9648788799e2233224c2271e1cad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8682561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e434eb454380e73e7c44d7ca5c460f16a0360b4819ac4b8c4ac88ae7a8bbcfe8`

```dockerfile
```

-	Layers:
	-	`sha256:24cc25e47f0f16d445c008dc5fbf1c80f2faa21d70cbc475e28c79c367bec485`  
		Last Modified: Wed, 13 Aug 2025 00:23:26 GMT  
		Size: 8.7 MB (8664532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff001ecf52a98e128c66fb4db3576db79384916cf1fcfcd26e6d1639e88a0763`  
		Last Modified: Wed, 13 Aug 2025 00:23:27 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d874e6a96dbeb2ce3f0fddc33230a2e0c86a5efc16e655f1fcd165a82ddfb204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.0 MB (374975866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030d02100bb425416fb054e074aeb9d563e726108f1aa981af3fe4efcc62efac`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 09 Aug 2025 00:48:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_VERSION=25
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be873d6dbdfc1f6d0b08d25149e5affd9c9fa1f6d932fcfd9dc52cfa2b99c79e`  
		Last Modified: Thu, 14 Aug 2025 00:23:32 GMT  
		Size: 17.7 MB (17727122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a28272b242530adb5426b84ab7d86f0c6ebe8ee789afc7694a42535c791748`  
		Last Modified: Thu, 14 Aug 2025 00:24:10 GMT  
		Size: 221.0 MB (220969444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:031b3906862b6adb9348e1b0ece6ac2480a59e54a6d65a0bac3f7b24a7a712ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8819526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265fe13039c0029c1567004775368a1c967634745454d9c7e5e766d9476bbcaf`

```dockerfile
```

-	Layers:
	-	`sha256:6dc67c061798c3d2d26f2d89aafd88c23d78fb60e0e2c90b40645c7507056f04`  
		Last Modified: Thu, 14 Aug 2025 00:23:23 GMT  
		Size: 8.8 MB (8801377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45aa1016b38014fe6432e4a24de415dbcb92ad853df4842c6831f3566fb390f9`  
		Last Modified: Thu, 14 Aug 2025 00:23:23 GMT  
		Size: 18.1 KB (18149 bytes)  
		MIME: application/vnd.in-toto+json
