## `openjdk:26-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:6e11b6682d30030d8ab5660c2809b5430719f8d48903ee1cb7d8f48bef3d81f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:3d29a2404ef640e4483f753f5daa7a2278f77ca6a291163a1a4501315ef9b95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255599949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a41297919fa6f2048c2e2dbc0360199456b797c25b875fb65c518b288d7a54`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42726a7998122b312235b60a36a189d9a34cb01ef01780968f29735519299be`  
		Last Modified: Tue, 02 Sep 2025 17:24:03 GMT  
		Size: 4.0 MB (4027245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d50c078aeda72c21013cc96fa77e48e08d22b514c1f952f3b4bc6c1f499c77`  
		Last Modified: Tue, 02 Sep 2025 18:28:52 GMT  
		Size: 223.3 MB (223342449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:dbaa452f8b9fd343d84df6ebf7ce8436b7ba0895ab71f4cccdaa6757a3c82981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d78cb35e80a137ffa99d435ce3e7768c072791e541a216199e1f8a510ad017`

```dockerfile
```

-	Layers:
	-	`sha256:1c30ac9c5ed0730afec48ebb877e542f228ccc90198d778f9b85289b63902c09`  
		Last Modified: Tue, 02 Sep 2025 18:24:20 GMT  
		Size: 2.7 MB (2650833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8c4ad2db1b74de55d3157d10b010c75bfa63c9a8d82812b8d187fe1a6c2713`  
		Last Modified: Tue, 02 Sep 2025 18:24:21 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cb8985de07a725d015303cc7798427920d41fff10fe48ae7111b6c9423fcc457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253071707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad964b5330067d502477b38a27f9e3648ff1b6322bafff65cccffd28c603a39`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
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
	-	`sha256:40779e99359615876c70cb21f2d350381823e6947e61b128f776c49c3e3227fc`  
		Last Modified: Tue, 26 Aug 2025 11:41:00 GMT  
		Size: 221.1 MB (221138326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:75a121b0044f7fb397e1b1aaa9ddcecffb12b60cc4567568f1340c3a6904dcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8791732b2f1f5c95990ed04dd88995774b2b6909c88010f09aec6bf345fdf085`

```dockerfile
```

-	Layers:
	-	`sha256:83401680727bf92d23728e9d12b02c292290d939da2fc08983f1ede77cef11ba`  
		Last Modified: Tue, 26 Aug 2025 00:24:21 GMT  
		Size: 2.7 MB (2650491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d62b61872dae8499321cc57842092eab3711144e389cc3c51727ca7d572d15`  
		Last Modified: Tue, 26 Aug 2025 00:24:22 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
