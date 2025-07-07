## `openjdk:26-bullseye`

```console
$ docker pull openjdk@sha256:9abc419c797ce5e85229fab65b7901c089144544cd5db4436ae43bc10ca4e5a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:73d16802b20bfea24bc80da3f056e49c0690278ea26263fa366af086819f2f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361391628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9614d354d7dfe277ce39fe95a4d499915fa1b8264937d8a921031044e0ba13`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452077c941f10849eea8a5ccdeb96fbbd41ca5b7eb6772161cb52baa1ac30139`  
		Last Modified: Mon, 07 Jul 2025 20:59:56 GMT  
		Size: 14.1 MB (14073127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622c1d4f56fd4069242bc4158d4575b49eb15deb81e90c7ebd7d369ecdef9b9c`  
		Last Modified: Mon, 07 Jul 2025 21:41:52 GMT  
		Size: 223.0 MB (223040862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:86916d6424fda9243a85d909fe4140563e30eeb85b4f2ac0bc3e23352759d42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4448eb9a611d369918b86836ad5f8e3d8a5cd07e6530dfd90c5fc054fe90f0df`

```dockerfile
```

-	Layers:
	-	`sha256:908069d3c4f35d0d57750bac8a6382821696fef8bacaf68b81c3aff2479c7468`  
		Last Modified: Mon, 07 Jul 2025 21:25:11 GMT  
		Size: 8.6 MB (8590824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b46ad048b7fd4e4e0253dc9770df3dfef1d944e13c70326e819b2f619249d34`  
		Last Modified: Mon, 07 Jul 2025 21:25:12 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4b6ce81229130801210cf20bde05887e369e46edbdae571e94ad9afd6533ddc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359144896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d33eb5a1605d6db27754302e8358bd8c7b2fa23ce2ad02318c8f9a89cf1a9f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 28 Jun 2025 00:54:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+4
# Sat, 28 Jun 2025 00:54:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='49aa2a8f29bd63727be9ab8e279ffceba2ee6d09beca9d221a69784da673476f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='529cc863c692cfa63afec612e73bdb9f2d8097a509454664315649e9955a16c2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df06c90ef797a08ca130b4072b43aed5e0d468ba07437357b47120c47fe96a`  
		Last Modified: Tue, 01 Jul 2025 17:43:44 GMT  
		Size: 15.5 MB (15527566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d320a69d7cd667bb39f3d155ad16ba8bb3edff4266ccbb44fabb219937bf068`  
		Last Modified: Tue, 01 Jul 2025 19:14:22 GMT  
		Size: 220.8 MB (220758638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6e47c99353c3bd9fa93fc632aa7a3da0cb88b8d48c747f99211f89cf91f1db9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8710530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467ea0617472f59739558d427482f334ddc614042eb6171acd5a3cb834f9affc`

```dockerfile
```

-	Layers:
	-	`sha256:93a6a9db46600bd09b399f3c76d227079d99cb37c598bb6aa67ffa2d53f797ba`  
		Last Modified: Tue, 01 Jul 2025 18:24:25 GMT  
		Size: 8.7 MB (8691787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a0791abd41ca6afcf9fc19e249f66941e5c67c94983db45f0581006823014fb`  
		Last Modified: Tue, 01 Jul 2025 18:24:25 GMT  
		Size: 18.7 KB (18743 bytes)  
		MIME: application/vnd.in-toto+json
