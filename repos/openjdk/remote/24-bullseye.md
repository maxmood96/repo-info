## `openjdk:24-bullseye`

```console
$ docker pull openjdk@sha256:9f93450bdb75236b12ca37ca16dd1024bc11c2a4beec24e109c7aee1f5c5f54b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:0ac923d3bb13f726080d64b04a8ac56863caf34f7089bce79941cda55165f1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351782761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb5862dbe7151de4b2529f5af866f49ad30e2e68c40d5f4db4a4eb14b756d27`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88092df2436b4adb5eb40fc42c8d527c8f897f9a9d4e11696956715ada3b461f`  
		Last Modified: Mon, 04 Nov 2024 23:07:43 GMT  
		Size: 14.1 MB (14071338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548fef75f9841a716baf6ba597aacf3ad82814ed215c1d5e1dcfb411c5dbf256`  
		Last Modified: Mon, 04 Nov 2024 23:07:48 GMT  
		Size: 212.1 MB (212143211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9cd4a4b9b38f7b1663c1e67c3cf77d036880cf478509f62bbb22d7d1f8d75d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc79eacbefae5e0dff4b102d6e4242e50567a7a959021fbe5a023dca1998d7a`

```dockerfile
```

-	Layers:
	-	`sha256:25135d1c7a13dc8206ea8565e487837bd9aa8e47df1c489842ca9324106919d5`  
		Last Modified: Mon, 04 Nov 2024 23:07:44 GMT  
		Size: 8.4 MB (8355822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517bbd7cf8a6765adecae63b43ca40246a5554fda7a7da3c393a2b09b8c3f98a`  
		Last Modified: Mon, 04 Nov 2024 23:07:42 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f0d8e4f3eac4e2e31180e7ec8ac033fda49a6c2b5a82fdd1e9ac7a856bb1925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350263420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a6485d35ff6c1f7f1662decee362c343158d76b6cc313afd13c618f31b7141`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 25 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c67029681a2f1c745c3a73366080881b2d349b4ffb9ce6a4e1e4b2c423555c5c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='3850e8de3f5cc9a22fabc0963a04d6205a9f242cf2cfc0d67a4399a54deb725e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d527fbd9717ac9c459b465835a094e9e4d86f9a7667769e0bca7bb0238260873`  
		Last Modified: Fri, 25 Oct 2024 23:03:17 GMT  
		Size: 15.5 MB (15526063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f757205edc3d2f888761074ea5714a9d6678e807f25171538acb252eb6aa28`  
		Last Modified: Fri, 25 Oct 2024 23:03:21 GMT  
		Size: 210.4 MB (210422015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ee16271f3f74691689a8e6d97af36970ad22efd13a0da4706fcef6dc6e2a914e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8475061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde3c69ad2aeb0d53c849ec4063df6a4d697756fcba79fe5ae597284e74b01fe`

```dockerfile
```

-	Layers:
	-	`sha256:b1cbef82b0ac5836f620ba0f58e87206fb79529cbfa1f0b53f1e6c058b7a9af9`  
		Last Modified: Fri, 25 Oct 2024 23:03:17 GMT  
		Size: 8.5 MB (8456283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a4f5db1291e66b0d6b3deea92256d4171a8e74e83c97cde4c9fb29bcc35e537`  
		Last Modified: Fri, 25 Oct 2024 23:03:16 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json
