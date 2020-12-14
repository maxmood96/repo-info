## `clojure:openjdk-16-tools-deps-buster`

```console
$ docker pull clojure@sha256:ce3ed36caf8e8ee3653ad5df545263c89707974eb70709058db2bac1b0c98a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-tools-deps-buster` - linux; amd64

```console
$ docker pull clojure@sha256:aa642ac48578eecd34fce838cc79b67c98bbf4b461cf42cc9e926b3f1f75bed6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350099079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63bd213df27a17b7258492bc916f7f0017719d2db8bab49fe06b9f859fc9b15`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:37:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:37:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 20:37:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 12 Dec 2020 12:41:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 12 Dec 2020 12:41:57 GMT
ENV LANG=C.UTF-8
# Sat, 12 Dec 2020 12:41:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Sat, 12 Dec 2020 12:41:58 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Dec 2020 12:41:59 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Mon, 14 Dec 2020 21:28:55 GMT
ENV JAVA_VERSION=16-ea+28
# Mon, 14 Dec 2020 21:29:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/28/GPL/openjdk-16-ea+28_linux-aarch64_bin.tar.gz; 			downloadSha256=ec5240a695751612960e7459476c6081e69a03aebe4ff3c7ae964b9235dfe9a4; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/28/GPL/openjdk-16-ea+28_linux-x64_bin.tar.gz; 			downloadSha256=2c2f2136a72e53deedef4e4e35d3d34315093a16732b9d112297e11e0661ea05; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Dec 2020 21:29:08 GMT
CMD ["jshell"]
# Mon, 14 Dec 2020 21:54:58 GMT
ENV CLOJURE_VERSION=1.10.1.754
# Mon, 14 Dec 2020 21:54:58 GMT
WORKDIR /tmp
# Mon, 14 Dec 2020 21:55:14 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1c623dd76ea75cb89623ffc71a5ec59297c785c0c19fc5c2fa0fe9428efe8a3d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Mon, 14 Dec 2020 21:55:14 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87cd3c61e278307eaa282fdbb51a5e2415cda64999c70a381ed6c5c724d370a`  
		Last Modified: Fri, 11 Dec 2020 20:44:17 GMT  
		Size: 7.8 MB (7811925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a3c799ec372b93b6dbd4b270effd9f36444dc164e8827ea9ab7aa0d1ef87da`  
		Last Modified: Fri, 11 Dec 2020 20:44:17 GMT  
		Size: 10.0 MB (9996419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c38f966ac77bd84d7866db24e1f7611b158e51e10e2e73ce009c3ad73f472`  
		Last Modified: Fri, 11 Dec 2020 20:44:36 GMT  
		Size: 51.8 MB (51830085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef1db7b21684606eef19063a56bae7c9d68753fbc1107e17f99575496ae353`  
		Last Modified: Sat, 12 Dec 2020 12:48:36 GMT  
		Size: 13.9 MB (13920271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6805247ef8e1b61f77bdd52608dc6ff58de57e39de9529d09778b294c603d04`  
		Last Modified: Sat, 12 Dec 2020 12:48:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9635a6f8eb9ba48301cbcb950abed66f627efeaeae9493f184bff9a2add5d5d0`  
		Last Modified: Mon, 14 Dec 2020 21:34:15 GMT  
		Size: 184.9 MB (184942158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d1db329a324dff5d4068a560df8206f1fe4533582ba6fd5780ae5d587bc176`  
		Last Modified: Mon, 14 Dec 2020 21:58:34 GMT  
		Size: 31.2 MB (31200282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
