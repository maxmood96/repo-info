## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:79dc8d6cfdbf78af9badea8abf9e06353c29a6f77a052c7070b45d8da6e3a012
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d8c576967b382a1da0c1359e7a485400c87cc88b54fcdc8002b5b0414748c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278076181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c56e162c3275eaae74ce28eaeffd7e6def67358dda27aec9d5a4f39a59b4bf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7d760ad2fe664c6995a4d9508e389d78b6bdf1b1f154b4a216d0fd3ad9a46bc`  
		Last Modified: Tue, 10 Sep 2024 01:03:41 GMT  
		Size: 51.3 MB (51293960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e0ec96c6f6dd610e84f939f57beb6b5f88042bfdfd41cca575894116639daa`  
		Last Modified: Tue, 10 Sep 2024 01:55:05 GMT  
		Size: 15.0 MB (15040872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0be31aa9df52a4f7dd566a79643749514500816354299a0f723afc852e206`  
		Last Modified: Tue, 10 Sep 2024 01:55:09 GMT  
		Size: 211.7 MB (211741349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1cf8ca03e4a6e698d04dd01e60a31229a26baf2225cd85af747ba4b1f1269d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9616d9f0f33f08da22169d96c14f7427747d62c429fecd9594f39041f3586a6`

```dockerfile
```

-	Layers:
	-	`sha256:3a7be50ee60b36b9a83869814bc44e8848d12be267dbce3a096fe3c9a3d89894`  
		Last Modified: Tue, 10 Sep 2024 01:55:05 GMT  
		Size: 2.3 MB (2287189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5084ff4d321f1f2bbad1cad9d96b39fb6b5ccabdf08739a923c30f7b1dd745c3`  
		Last Modified: Tue, 10 Sep 2024 01:55:04 GMT  
		Size: 15.4 KB (15400 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dd06879ede3dc88da4aa2965d5cba81c8e00a608939f78d11c3617762492146c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275344834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c220a01ee2c046804f17a4be39055fde664973111bdd2e2ebf34293331b9ab7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:26021d1fe840c0392b944d95d8144754412f70a5f838918b647f05d3328586c0`  
		Last Modified: Tue, 10 Sep 2024 05:36:16 GMT  
		Size: 50.0 MB (50007854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50829b315adcf131e7f517cf1be3bdf1e989b87efc9d19f191cec6dee06004ea`  
		Last Modified: Tue, 10 Sep 2024 06:44:36 GMT  
		Size: 15.7 MB (15702969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f84aed04c9313d49f4d5165de6824a2230db60374ee7b119122a6cdeb3b83af`  
		Last Modified: Tue, 10 Sep 2024 06:46:19 GMT  
		Size: 209.6 MB (209634011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:77bba0c41477afc2c52b2d699a828b91f83a782f97499947254bc74fc9e5c379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651755b00bb4ddbc69f17f54184a0007dd090827a5633c29dca203d60e590e07`

```dockerfile
```

-	Layers:
	-	`sha256:4d999d0572c529e3168d64fb5b57beb0de26ef2bd24e8988d62388ead18922b6`  
		Last Modified: Tue, 10 Sep 2024 06:46:14 GMT  
		Size: 2.3 MB (2286634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2493a7fd3e0d27fe54a293a9529e8f324c5b900563caf7daa18604ed6eacebd7`  
		Last Modified: Tue, 10 Sep 2024 06:46:14 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json
