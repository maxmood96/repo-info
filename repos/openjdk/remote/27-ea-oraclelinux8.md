## `openjdk:27-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:a68989c8b1e4b1edb6a304962bbfbddefde9d1fdc09e3a010d01b860be3bf551
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:8896d57819e262e592ef908cdfa2a2211acf283bb1ec594e1ed17563e12a0248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295227314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34c2532ab2255ac544fa44166ee274c0b12eedd397c008be313f5e6eec22f0f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:50 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:50 GMT
CMD ["/bin/bash"]
# Fri, 13 Feb 2026 00:01:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Feb 2026 00:01:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 13 Feb 2026 00:01:18 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:01:18 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:01:18 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:01:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:01:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df558405081e8d5c6af13745e322e2d270802ff99fe9a1eea2b63615844efa1a`  
		Last Modified: Tue, 10 Feb 2026 23:03:01 GMT  
		Size: 51.5 MB (51464982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bd0731175e68b6ef68a1dcbc9f6d0344ad1fb2562f3249da574ed9673c5550`  
		Last Modified: Fri, 13 Feb 2026 00:01:39 GMT  
		Size: 15.0 MB (14991342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cb11d265fa98c403bd42c6df7ce0ee712c1f4b3b201d57e746fb2aefab7598`  
		Last Modified: Fri, 13 Feb 2026 00:01:43 GMT  
		Size: 228.8 MB (228770990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:72262fcde68beea3d8f2e483a6b77dd089858c9c8181cb2a87b3333d5bece82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c528f4d7f528cfbff01ee36bcd863509cfe43f722ae98090834462ab4b979c8`

```dockerfile
```

-	Layers:
	-	`sha256:d9d725e5ff8e7cd592ae2e26f14528851fd9b6a6bfaafa09bc6480dbdb9c649a`  
		Last Modified: Fri, 13 Feb 2026 00:01:39 GMT  
		Size: 2.4 MB (2448066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a5519fdf3e13e9eff3cd2018cdd5978ef60520366b11afd399b2832c10225c7`  
		Last Modified: Fri, 13 Feb 2026 00:01:38 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a3998b40a85b5d01e5bbf4ee16bb3f922154fb2450121e7d2c5d19306d32a169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292620124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b68ac88d97bba04d18c51783a943719a034bce02b0fcbafe43263ff1964cbd0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:07 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Feb 2026 00:03:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Feb 2026 00:03:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 13 Feb 2026 00:03:24 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:03:24 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:03:24 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:03:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:03:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07a1effc9605f90c3e2f6e8e5b85d7de94a80b436a975fd605cfe7f53acd6ca5`  
		Last Modified: Tue, 10 Feb 2026 23:02:19 GMT  
		Size: 50.2 MB (50191339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6191d6a524d10e1eabcb0c301cd2a8c223e8b0882196d509f219b528651ca`  
		Last Modified: Fri, 13 Feb 2026 00:03:46 GMT  
		Size: 15.7 MB (15690725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1f6be38ce13a8c3f1917b8b132a6ef76005f4d5aeea31bbabebeffebef8f7c`  
		Last Modified: Fri, 13 Feb 2026 00:03:54 GMT  
		Size: 226.7 MB (226738060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:0d364615c73822a321171da7906ac23ea0c4f9ec637ee4b7a909787001056f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86b1e5cfa298131c32cff77260385f07850f9ed7a8dd804922a40b4130620b1`

```dockerfile
```

-	Layers:
	-	`sha256:43ac6a95b3bdbb0f25c1ff0ef512f611448831b5b1b460566357c5b1a25faac3`  
		Last Modified: Fri, 13 Feb 2026 00:03:45 GMT  
		Size: 2.4 MB (2446876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a06f548fd5d4f2aa62b7c5fe3d79a5cab1d95b0ba4d550ebcfd289ee7ed3236a`  
		Last Modified: Fri, 13 Feb 2026 00:03:45 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
