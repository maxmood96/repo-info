## `clojure:openjdk-19-tools-deps-slim-bullseye`

```console
$ docker pull clojure@sha256:ef386e06b136e8d1ab1a01ecf4f0dc96c1b40dafcb5c6366bf9e4a2fd5da165c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-tools-deps-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:feb27206712596ff2d05ce87aaf7d8f01e650427cbb99f889ba8ba85e18f6e2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286438822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ac831a3344681e0e3b2f3e25b1ab6fb42dfdd25897c09a72a17e5be8475bae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:21:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 14:21:07 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 14:21:07 GMT
ENV LANG=C.UTF-8
# Mon, 14 Mar 2022 20:14:51 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 20:15:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 20:15:05 GMT
CMD ["jshell"]
# Mon, 14 Mar 2022 20:46:44 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Mon, 14 Mar 2022 20:46:44 GMT
WORKDIR /tmp
# Mon, 14 Mar 2022 20:47:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 14 Mar 2022 20:47:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 14 Mar 2022 20:47:01 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 14 Mar 2022 20:47:01 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Mar 2022 20:47:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8366d5a4a5f71bf009ed651eb5566bf81bcd61ddaa4a2541fc65505bb076ca`  
		Last Modified: Tue, 01 Mar 2022 14:40:45 GMT  
		Size: 1.6 MB (1582090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742acb3c151b7dcc899c93aecfd3071182a72f9e4a2b948c348fc72b00819b51`  
		Last Modified: Mon, 14 Mar 2022 20:23:36 GMT  
		Size: 193.5 MB (193458806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dad19df13d3f50e0f8cb3fffb26cb12790d676025a166415eb3c72842957220`  
		Last Modified: Mon, 14 Mar 2022 20:52:18 GMT  
		Size: 60.0 MB (60030503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a732056640dfd55591e80733d1f99e6c8ab4b1f70354f5e0a8fcbf7c462dd80`  
		Last Modified: Mon, 14 Mar 2022 20:52:11 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbc48b2a791a409f51d54695539090afd9296f6c2955b70c122687ea079e612`  
		Last Modified: Mon, 14 Mar 2022 20:52:10 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-tools-deps-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7680e1c209cc16e99bac3aa09c26a250c5f7c696d19b9bfa04512ff812e13b6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283858365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a828b3d52bdfdb6d31e17250f85f61afd2cc6a2aaba8c5381b715d2cd08adfd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:48:14 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:48:15 GMT
ENV LANG=C.UTF-8
# Mon, 14 Mar 2022 19:05:56 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 19:06:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 19:06:15 GMT
CMD ["jshell"]
# Mon, 14 Mar 2022 19:59:07 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Mon, 14 Mar 2022 19:59:08 GMT
WORKDIR /tmp
# Mon, 14 Mar 2022 19:59:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 14 Mar 2022 19:59:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 14 Mar 2022 19:59:26 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 14 Mar 2022 19:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Mar 2022 19:59:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee4a8201309b4b9bb0e0e0efc8d45265ae39d932512f5edb149b65eaf107d9`  
		Last Modified: Tue, 01 Mar 2022 14:12:59 GMT  
		Size: 1.6 MB (1565936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b73f5fd6d754d54fb63d39608eab646b182489072fb9881fe0f42ed90d48d6`  
		Last Modified: Mon, 14 Mar 2022 19:20:43 GMT  
		Size: 192.3 MB (192280109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0377970fabcccc72897f211921325d1e38c3a9b71c047bc6f12fcb9d0244af70`  
		Last Modified: Mon, 14 Mar 2022 20:08:49 GMT  
		Size: 60.0 MB (59954283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4995b779447fc60c3e376df49c263d8fc52152e54542645afb5010920ea8eb84`  
		Last Modified: Mon, 14 Mar 2022 20:08:40 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c9b4e1b5e37507e9aa07fb72d7820419d735f458db2fdbe21050cd8b2b5477`  
		Last Modified: Mon, 14 Mar 2022 20:08:40 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
