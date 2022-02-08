## `clojure:openjdk-18-boot-buster`

```console
$ docker pull clojure@sha256:646b7050aebdfd2c59a605d57d39b78ba605f8d168cc90f56a0a8ef902033bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:292aa45b5abd582ce124ed80ef8df1113a932bed18e936eaadaa9fceb637f7cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382527099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b712e2417a1bb42daa85b8a679adfc104b6838543c871cb598dd7be90cf5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Tue, 08 Feb 2022 06:08:31 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 08 Feb 2022 06:08:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 08 Feb 2022 06:08:32 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 06:08:36 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 08 Feb 2022 06:08:36 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 08 Feb 2022 06:08:36 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 08 Feb 2022 06:09:01 GMT
RUN boot
# Tue, 08 Feb 2022 06:09:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 06:09:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 06:09:02 GMT
CMD ["repl"]
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
	-	`sha256:9a9ce05bfcd99eb451a29bb99d77b21e00b3d1a1a95733fc17532b86a3b51d4f`  
		Last Modified: Tue, 08 Feb 2022 06:18:09 GMT  
		Size: 903.8 KB (903825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1e432ae95325548eee4cf4ae886513b4c83d75e5667ab403e3ca057971116c`  
		Last Modified: Tue, 08 Feb 2022 06:18:12 GMT  
		Size: 58.8 MB (58820579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d931f0f9b3797283c944d2848cdde995f35757260774757e71fc7c8332bc0f8b`  
		Last Modified: Tue, 08 Feb 2022 06:18:08 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d4eb28481149366c44af9e34a00c6bfa9a1ef7b2259b81abcfcd2dc06978a3e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380707957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf51f51fefa33a3a44209f8c82e097984b92a078cdca279e5aacc183d81809a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Tue, 08 Feb 2022 09:27:15 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 08 Feb 2022 09:27:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 08 Feb 2022 09:27:16 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 09:27:26 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 08 Feb 2022 09:27:26 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 08 Feb 2022 09:27:27 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 08 Feb 2022 09:27:40 GMT
RUN boot
# Tue, 08 Feb 2022 09:27:41 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 09:27:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 09:27:42 GMT
CMD ["repl"]
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
	-	`sha256:63c4d5ad61f85575914080645bd71837b7e2c7615ec7f31c647ef9daae31b974`  
		Last Modified: Tue, 08 Feb 2022 09:39:04 GMT  
		Size: 663.8 KB (663798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5938c768d813fe48a1fd0c2b03df5dd7495423ebb93817d577d4f2de1a914e6`  
		Last Modified: Tue, 08 Feb 2022 09:39:09 GMT  
		Size: 58.8 MB (58815339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9995e2eab9fb15dcd917b0d7e0ce251fdf1f0d530d3bcfdc34627b0a7cc266db`  
		Last Modified: Tue, 08 Feb 2022 09:39:04 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
