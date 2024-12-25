## `openjdk:24-bullseye`

```console
$ docker pull openjdk@sha256:75cf3b076c900c516badbfff9e3f0ceb303a7205b26952c7c2fdf5b9090dc47b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:468026b1209843c1dd78a6b3c13d37866ef85d7820f6d37381df01db03480f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350977905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c12162bbbf995006949c654639768817f570702498b755bda8b35723976da8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5d6cd498b928e21a189013e7471228b4d3cae33f0df5d56eb805cdb638aed4`  
		Last Modified: Wed, 25 Dec 2024 00:13:57 GMT  
		Size: 14.1 MB (14071481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8d9bd16ea6cd52e2efeab647d1adcfd6974c18b474fd96dff265ca9b9ccf3a`  
		Last Modified: Wed, 25 Dec 2024 00:14:01 GMT  
		Size: 212.9 MB (212855466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7fe131eebeae94500c2581a1a5d5c9a634de52fd41469a4a02ba8bedf58a1884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e7d1daf6be0c6629c462c296b66728e2640dea54f4fbdea7ee19e8e955f9d`

```dockerfile
```

-	Layers:
	-	`sha256:f6c4a1e7ca1e6dbb1c74b31a4a6eadc5ce315551c20c6fbbd968a5e16e74cdde`  
		Last Modified: Wed, 25 Dec 2024 00:13:57 GMT  
		Size: 8.4 MB (8364785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b2a061a6c25b28b8b9aa7f430b9305ed59c6da6609282ad8bb7001bbb8880fc`  
		Last Modified: Wed, 25 Dec 2024 00:13:56 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:45965b13c1125c4258251bd7d493b151640e61fb126a265d2f61af87b85db7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348980488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f661e7366fca60971daade6deb9310e2512cc948ee624ef19e91c520b49f32d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43843d4db248bd55b162c50c092e0af24e1906957688ece77c8fd78e7c62441`  
		Last Modified: Wed, 25 Dec 2024 11:59:36 GMT  
		Size: 15.5 MB (15525945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fbae9358bda254896a67b0861955b034a93af3306c84fe92127bde9bd716ec`  
		Last Modified: Wed, 25 Dec 2024 12:01:31 GMT  
		Size: 210.8 MB (210812396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4a92ecb3fc6e009556922b9036579f2d6b0985ff7597839cbf5fbab0cccc857d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8484508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e1ba3271d6373cd8e5d6f6e5f39c8d758798906e5afd759ad61aeb86667ffa`

```dockerfile
```

-	Layers:
	-	`sha256:8bd6774e6649795dab83681691cd397491da08aa60263912051802c5d90fe4ed`  
		Last Modified: Wed, 25 Dec 2024 12:01:26 GMT  
		Size: 8.5 MB (8465747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bfc534931f9d1502457f927f1327f384750df6984a9c99731bc6539799437b`  
		Last Modified: Wed, 25 Dec 2024 12:01:25 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
