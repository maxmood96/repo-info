## `clojure:openjdk-18-tools-deps-buster`

```console
$ docker pull clojure@sha256:748d6e925fda10e6d487526a3d30d5874ec5b6ecab251ab2fba452d6b8f88d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps-buster` - linux; amd64

```console
$ docker pull clojure@sha256:3522571848a3577fd1c8ba31e21caf5f31ffb94ff71c6b0aa00ea47962866257
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354028180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498e21ba6b166341c25581aaa470e8db797ad7bd7b7d3e7e74d80186c60a4e56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:47 GMT
ADD file:a290acee3581e1e9c42c0a37b53086a8f070cb0730179be81a6ba24a620b6ee4 in / 
# Wed, 26 Jan 2022 01:40:47 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:20:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:20:51 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:20:51 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 03:46:12 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 03:46:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 03:46:24 GMT
CMD ["jshell"]
# Tue, 08 Feb 2022 06:09:29 GMT
ENV CLOJURE_VERSION=1.10.3.1075
# Tue, 08 Feb 2022 06:09:29 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 06:09:40 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a6b72c9b23d348a0636813c5f59db5dda622e3b8dbb86124cbb51e3aced714d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 08 Feb 2022 06:09:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 08 Feb 2022 06:09:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 06:09:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 06:09:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a024302f8a017855dd20a107ace079dd543c4bdfa8e7c11472771babbe298d2b`  
		Last Modified: Wed, 26 Jan 2022 01:47:01 GMT  
		Size: 50.4 MB (50437057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289773030fdc98afe6cc53bdd0c05332ea8ff21ad836afa1d3042388953c43f8`  
		Last Modified: Wed, 26 Jan 2022 02:23:32 GMT  
		Size: 7.8 MB (7833856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb8b3399fe8dd0b83bd5e32a97e5183ab235d6fb4cc0b5dfabb20e6653e715`  
		Last Modified: Wed, 26 Jan 2022 02:23:32 GMT  
		Size: 10.0 MB (9997205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c63da771697b362929cecc84777e8cfbb716ff3d575b999854d83ada039b695`  
		Last Modified: Wed, 26 Jan 2022 02:23:53 GMT  
		Size: 51.8 MB (51839910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c88c63b5d1adc4c1a364370b244e9b042b780d79deb1240bd7dc938953636b`  
		Last Modified: Wed, 26 Jan 2022 09:42:29 GMT  
		Size: 13.9 MB (13921285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca4bbab77cc862a9f1046eb2204569a7ffa5471f4fcf26c83af63477ef9c5e`  
		Last Modified: Tue, 08 Feb 2022 04:00:46 GMT  
		Size: 188.8 MB (188772975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5aa1a035485f26b7f4e8afcded8a615e906cad6537f1df8c81b30707daa973`  
		Last Modified: Tue, 08 Feb 2022 06:18:45 GMT  
		Size: 31.2 MB (31224862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95d15ded20089fa3c4a28978513ee015630011f38bebad8e99d3607e8158e8b`  
		Last Modified: Tue, 08 Feb 2022 06:18:42 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c89873493f22cdaae3830d09603ecb8bd37d5307436dad0c6d826353d3a0f14`  
		Last Modified: Tue, 08 Feb 2022 06:18:42 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a537f15bd6ac781758229c11565c4a9acfe42acb804dd9ed3f9c0b101f0478bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351796170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd1b9ae9d1723cbf47aca2b8a18d3af553a484bb2e642b0286ea28745104fac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:41 GMT
ADD file:98a75269e438ff15cee16ad2763fe2698fb436bc4770c0ca27c059f66b65e56a in / 
# Wed, 26 Jan 2022 01:42:42 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:14:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:14:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:52:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 05:52:44 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:52:45 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 06:27:37 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 06:27:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 06:27:49 GMT
CMD ["jshell"]
# Tue, 08 Feb 2022 09:28:18 GMT
ENV CLOJURE_VERSION=1.10.3.1075
# Tue, 08 Feb 2022 09:28:19 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 09:28:35 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a6b72c9b23d348a0636813c5f59db5dda622e3b8dbb86124cbb51e3aced714d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 08 Feb 2022 09:28:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 08 Feb 2022 09:28:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 09:28:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 09:28:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ccd458f933f7966e412773ee1551aaf2433a5bf9adaae519e2ac7c9c3f8b5f89`  
		Last Modified: Wed, 26 Jan 2022 01:49:28 GMT  
		Size: 49.2 MB (49223041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3524e6d2c855bef1f32da73e00738b2e5e91e6a346d19f8b33e8e8117c82748`  
		Last Modified: Wed, 26 Jan 2022 02:25:05 GMT  
		Size: 7.7 MB (7695112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cc9cf00cd9023559aeda43668c7d9d621318631bab103ae03b8a3787260048`  
		Last Modified: Wed, 26 Jan 2022 02:25:05 GMT  
		Size: 9.8 MB (9767300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f0325e59cadc58f4e81c6a282319b0c01f54964ef989205974a6557cf15040`  
		Last Modified: Wed, 26 Jan 2022 02:25:25 GMT  
		Size: 52.2 MB (52168727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ba646f620fe2232a5e982cdc5a2ada5f58b4fd4a0ad57ae326484ee00b2308`  
		Last Modified: Wed, 26 Jan 2022 06:14:04 GMT  
		Size: 14.7 MB (14671090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55506e41cd868e0bf9d71c70a4e0914e70601ab927c6c40ac9694b387231e78e`  
		Last Modified: Tue, 08 Feb 2022 08:27:45 GMT  
		Size: 187.7 MB (187703144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be63b7edc06cae4254ecd1bbb44d7e923f88af8ebac24a566ee1fb8b048c0574`  
		Last Modified: Tue, 08 Feb 2022 09:39:45 GMT  
		Size: 30.6 MB (30566724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be03240cdf47a2b41c8d2b63c167c6581c3b69b4cc1733af491c7e2c994297f8`  
		Last Modified: Tue, 08 Feb 2022 09:39:42 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84defa00ac924f931c16f455b46f391fd9173ffba0cbfb554d2b59a10dfa3721`  
		Last Modified: Tue, 08 Feb 2022 09:39:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
