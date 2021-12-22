## `clojure:openjdk-18-slim-buster`

```console
$ docker pull clojure@sha256:0f385849db02223a0246694214538b3ba99aef4d2ee5f6cb9239ad3461834f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:67637616983ee8ede9e1e64edf2cb60bed23ae448bdf07bb39d7feef356e6aac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277875671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3b6d0911b75f752ad83bee2061604d1dd56bd2eeace9e135e65bb60a766870`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 22:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 22:59:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 22:59:58 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 22:59:59 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 22:59:59 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 23:00:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 23:00:14 GMT
CMD ["jshell"]
# Wed, 22 Dec 2021 13:42:06 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Wed, 22 Dec 2021 13:42:07 GMT
WORKDIR /tmp
# Wed, 22 Dec 2021 13:42:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 22 Dec 2021 13:42:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 22 Dec 2021 13:42:25 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 22 Dec 2021 13:42:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Dec 2021 13:42:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c983bcc370920d99695dc288c345343be841987206e4ce762a4e7599f28c96`  
		Last Modified: Tue, 21 Dec 2021 23:16:09 GMT  
		Size: 3.3 MB (3269567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f54dcb284410f41e55cf4f4ca250e28e480947f47fd02d4a206df1320d7be4d`  
		Last Modified: Tue, 21 Dec 2021 23:19:07 GMT  
		Size: 189.0 MB (189011832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfb7d5bc56296c5fd04926c794dd988aa477468a5645a8a70a2bfac315a1f3f`  
		Last Modified: Wed, 22 Dec 2021 14:00:33 GMT  
		Size: 58.4 MB (58439518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ef3b21bc3684f5515345de6fc20b3fab7131348ca5dd58ec3401772c04f57d`  
		Last Modified: Wed, 22 Dec 2021 14:00:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9872d59ccaff15f9b393c9d654f3682ca6bfed266d3d4302444eb28ab8b7b5aa`  
		Last Modified: Wed, 22 Dec 2021 14:00:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a0a7574eabc29e256028a6d0175e995245dd3d5b5aeb3f851892ae34247213d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274870625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9d1cffb8e47f8a31e3d80e6077975d0122c2471ac0e333174322ffa9b3089b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:56:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 02:56:42 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:56:43 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 02:56:44 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 02:57:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 02:57:05 GMT
CMD ["jshell"]
# Tue, 21 Dec 2021 22:13:07 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Tue, 21 Dec 2021 22:13:07 GMT
WORKDIR /tmp
# Tue, 21 Dec 2021 22:13:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 21 Dec 2021 22:13:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 21 Dec 2021 22:13:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 21 Dec 2021 22:13:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Dec 2021 22:13:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c74145b5f237a66007b7c0d55f2ffe3d54c07bf5e09c19bebd4ec94b00005e`  
		Last Modified: Tue, 21 Dec 2021 03:17:41 GMT  
		Size: 3.1 MB (3118854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db36813e8b0fa893cb2f9a2ceeede667700fac83259dcbda4848cedbd57cba07`  
		Last Modified: Tue, 21 Dec 2021 03:21:18 GMT  
		Size: 187.7 MB (187740640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3a5edfd462be0ad2ecfd84cc8da6843dd230bcd713d1c9de0686b9811656ad`  
		Last Modified: Tue, 21 Dec 2021 22:35:38 GMT  
		Size: 58.1 MB (58086953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def4a506a34cc8d589fc7def782443901faa3b08148bd206812c282540bf3b7`  
		Last Modified: Tue, 21 Dec 2021 22:35:29 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f323bc24578c0e3a951780cbb3009af3e7afec884ed6f64764975eb157e684`  
		Last Modified: Tue, 21 Dec 2021 22:35:29 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
