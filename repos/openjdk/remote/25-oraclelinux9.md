## `openjdk:25-oraclelinux9`

```console
$ docker pull openjdk@sha256:05a31350ada1fd6e31a51fa76efaa327435f34aee99c9306f7d95556bc2861e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:11c695634ff452cb27ae6215f65934bf5a5124060654ce2055bb0b9e95d44906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299593911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4093fa635abf4fecf60ba15aded9ea2fcc6e09a0074f1fcee14371ba8e378`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8195b1754dda782ae9f3927a8075b04b114419eed52b5da8f2338671a8a2bb53`  
		Last Modified: Fri, 25 Apr 2025 21:45:29 GMT  
		Size: 38.1 MB (38106170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7078a3db89f70533ef4c4c40fb197fab548e2748cc9c390f921b7a1d517316`  
		Last Modified: Fri, 25 Apr 2025 21:45:31 GMT  
		Size: 212.4 MB (212396531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:799c70468d05bac38b1c75e25e785bf17e723cf52f370e523174406217cff363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3644252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8c14618ca9411ee2f9fb8ca63a92d1606d4d5ec847cdd56cc389a5a34596c8`

```dockerfile
```

-	Layers:
	-	`sha256:0de8c3bffbe4963b345aaa4d813f8edca16d5bb859a1dbe28e5d6a62e3d8250b`  
		Last Modified: Fri, 25 Apr 2025 21:45:28 GMT  
		Size: 3.6 MB (3624506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b814a297b5968fc8005b40fa889ef684edcc66d48c56b051b8f036709435ff`  
		Last Modified: Fri, 25 Apr 2025 21:45:28 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:62e687590178503d5832becceab7dde129261a7eff86c39c32eb546de8e4a098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296409022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887f1185f414d488ba6e92d9b076e0676b616900da5357d9a23bcbe71620d823`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5750f1793fdd6894b80fd32af7c3dc7fd61fe28a4003df2c3b5206dfd9ecf575`  
		Last Modified: Mon, 14 Apr 2025 22:58:29 GMT  
		Size: 38.5 MB (38500787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440c14d9a9c065fbf79a54e624b7cbdf94c42b80e092bb0b1d3ffd71f8c4ae9d`  
		Last Modified: Fri, 25 Apr 2025 21:45:04 GMT  
		Size: 210.2 MB (210233412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:dae76228f063172cee8a32541bca58fe12d8c5a39a9240d8be2022e11bde8c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ed2328c09a550d81cc674d9ba5d4789f2e8b6a17852f084c16d451362fc8d9`

```dockerfile
```

-	Layers:
	-	`sha256:1af76897024f100a9b834c571924e7d58955aac3fdcf1a534ef3f2e12925bf29`  
		Last Modified: Fri, 25 Apr 2025 21:45:00 GMT  
		Size: 3.6 MB (3622268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14a63bfb353a58b4fef7290cc5af5fad67eac896d15e01821452a39e87ae6e00`  
		Last Modified: Fri, 25 Apr 2025 21:44:59 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
