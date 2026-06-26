## `openjdk:27-ea-28-jdk-oracle`

```console
$ docker pull openjdk@sha256:6312752b5355991f35a55e79394b00a78ca31ea991be5f8f673fb64345324f0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-28-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:838c67e1a0757bc4e4dbec79e3e8660c96c6d4de8ee71233a2333b65acffe566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307747895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18431bd64581bd24b277fac8672e46622621d2ec1bbdb9006d08eea70d85d0db`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:48:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 26 Jun 2026 17:48:57 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:48:57 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:48:57 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 17:48:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='45707add322e7be16c9eaf4e6f15febf5bd06baeab88aea73d3a89fae0d7bcd7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='1fe32bfb8b4a3533d1cbd2199cbdb9c62d72032b409da56d58135460a7e0c5a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:48:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0455190fdb45ccc9d93a25da8e29d77b0da722c4f8f224b86b5fca365a4ace`  
		Last Modified: Fri, 26 Jun 2026 17:49:20 GMT  
		Size: 37.7 MB (37687816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4060ac85090cb24e15b38642ee1561b7d2b2a9abe0c599227ef64eb8035de3`  
		Last Modified: Fri, 26 Jun 2026 17:49:24 GMT  
		Size: 227.0 MB (226979497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-28-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d2a5190e614df03797321ee113c01d7ead332578ce46932ea219082d061123c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f7439c1ad1ef70dc9d65f890dfcc9d9fc94297783692dcbb71fe957a90c41b`

```dockerfile
```

-	Layers:
	-	`sha256:4b22e7dc74bf977a7f35bcfb0cc20ddd7581bfcbb1ed78b0b50142007e0ecc8b`  
		Last Modified: Fri, 26 Jun 2026 17:49:19 GMT  
		Size: 2.4 MB (2366462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307c3486d788cac25129e7f947545da5f2652347cf0d5bbf648501d960d67c14`  
		Last Modified: Fri, 26 Jun 2026 17:49:19 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-28-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:92c29905cb1125c2d9dc233e0ec021fa574b57242ef656cd2a491cba998dd4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304136669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467dc22242253a64f444753660d86faba857147ffcf42e98cc8680cddbd03d25`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:32 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:53:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 26 Jun 2026 17:53:44 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:53:44 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:53:44 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 17:53:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='45707add322e7be16c9eaf4e6f15febf5bd06baeab88aea73d3a89fae0d7bcd7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='1fe32bfb8b4a3533d1cbd2199cbdb9c62d72032b409da56d58135460a7e0c5a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:53:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaf11ff807fb352a9672d40d243f01d7759a0f98dc198d7a674beee9736388a`  
		Last Modified: Fri, 26 Jun 2026 17:54:07 GMT  
		Size: 37.7 MB (37696223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7142e277aefbe192e79cf5264b4c3d692f4216955fc9e993246a5c89b28332`  
		Last Modified: Fri, 26 Jun 2026 17:54:11 GMT  
		Size: 224.9 MB (224944751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-28-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:ba846ddbb2243317faa65ca644c62ff6506697faec7a7f1afd2b0c21aa75ff86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9611a8a3f1a899e0ca94917f53b72ed8a91651e818920929e21e13cde34cefad`

```dockerfile
```

-	Layers:
	-	`sha256:ad708f8ce56ef39d5ad59b059e595633338eacae3ff7e15ad968dc80248d756a`  
		Last Modified: Fri, 26 Jun 2026 17:54:05 GMT  
		Size: 2.4 MB (2365990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da89d3127f6c9ec455f29c604ce1e928c93378cd5da673f8d99aef65ed474bd7`  
		Last Modified: Fri, 26 Jun 2026 17:54:05 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
