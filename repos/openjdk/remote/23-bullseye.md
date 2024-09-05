## `openjdk:23-bullseye`

```console
$ docker pull openjdk@sha256:66b654cf9d194f93635e78ef4b501ce97311499667769096e786d77ae18813c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:ca0b23280f47f3da09b1491d501a16d86883cb533ce5606112128addb5a08d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351035411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af9518addd15111f50da03526b3936b4eccb0a14d52b64ec3f98e28a463f6a0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88df6c704bc5200ffa357378517241d2103ea00dc3fefd0168b890231cb209e6`  
		Last Modified: Thu, 05 Sep 2024 00:16:45 GMT  
		Size: 14.1 MB (14071322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a1599dcc44f88cd90185dd6614a218c7b097a53ec14ec572f63633fc1026e`  
		Last Modified: Thu, 05 Sep 2024 00:16:48 GMT  
		Size: 211.4 MB (211392339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:065c73c2087eef43c8d4adcb14eb9637cd693ec0d9015d6b3d0c62179b5621ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8211120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d8dc932893029023dd0819515d6aef661049b877edd11b516492a7bb4c982b`

```dockerfile
```

-	Layers:
	-	`sha256:c944215fd15c835339aa90f26906986ac5f151241937e049f36da811945d485c`  
		Last Modified: Thu, 05 Sep 2024 00:16:45 GMT  
		Size: 8.2 MB (8193246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29e4eff5559ec75618647dc6c1cdfd0f094c2a6094e1ebb93f5ee7567e0bb1d`  
		Last Modified: Thu, 05 Sep 2024 00:16:45 GMT  
		Size: 17.9 KB (17874 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ec8da33e8a21628922b28923979c955e18314e7c6310a90c8e1da8c5320435f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349117717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9a59cb70c660ae2137abc7f1b92ed811ef175162f357ea7c01b6459b2c780c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1086d0a45bcfc1c6541cf22b33b3780a9c941b475782eef088d66d0c7596027`  
		Last Modified: Thu, 05 Sep 2024 12:59:49 GMT  
		Size: 15.5 MB (15526171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f411776291d3c131c221b9493faba576c9bbf33eaf9fa0c938cc93eb810e71d`  
		Last Modified: Thu, 05 Sep 2024 13:03:48 GMT  
		Size: 209.3 MB (209276766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:1dbdc22e5cac91304e8f840bee6fe21e68587473c556600e5b54cdefcec49deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fca3b6f30a4fcba6dfd9fa6feb5870d3abd52ee72d5e8eda7723f579682fba5`

```dockerfile
```

-	Layers:
	-	`sha256:e32c8e3360ed5a0243e69ced303e1f1d0d7b6c85141813db31f7388478f39360`  
		Last Modified: Thu, 05 Sep 2024 13:03:44 GMT  
		Size: 8.3 MB (8294932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9a852d8ebd87f288b9e530b8c04cbe001517b2df7e4fa486c53a07c8800e13`  
		Last Modified: Thu, 05 Sep 2024 13:03:43 GMT  
		Size: 18.2 KB (18191 bytes)  
		MIME: application/vnd.in-toto+json
