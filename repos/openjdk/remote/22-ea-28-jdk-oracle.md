## `openjdk:22-ea-28-jdk-oracle`

```console
$ docker pull openjdk@sha256:6269f9d1a733791dd8776e4ee4e03567af921bd33121dab4727e281636655b03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-ea-28-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:30df5926d378a4fd49dda2d9c500e14074374cad509cb47533330420da043541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269049226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a34c60d579042b956933d21214ef77996d1e6d4d88bb61806360f7b91db78a7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 15 Dec 2023 19:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_VERSION=22-ea+28
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='c19197168f6e8f67635539f348e7e97ebf21cacda670bec9304e59cb9e967fd1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='cfc0261560182c1fb0e8e6ab133a6300aa3da0663abdf5f195f7a664f8f7d56e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95b73374719b83d4c7901a3b18a3e4055f668eea079bd3b7cbce462781144a3`  
		Last Modified: Sat, 16 Dec 2023 01:52:15 GMT  
		Size: 15.0 MB (15003893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc1f74f0b45a37821231184f4dae8b38f392ac0a654f84423b990e07168464f`  
		Last Modified: Sat, 16 Dec 2023 01:52:19 GMT  
		Size: 202.7 MB (202725368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-28-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:542c823c00beb57ded2b7031d4d5b41869e4c22ebab8e158a3a1c710187be488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b18210427c0e4d4f35fe19d8952f153e6dd1f5f7d400491d12af12f0600ebc`

```dockerfile
```

-	Layers:
	-	`sha256:fc04e22181021765664482dc75242582493030997a90daec45b985d121bfa793`  
		Last Modified: Sat, 16 Dec 2023 01:52:14 GMT  
		Size: 1.9 MB (1915831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ccef4b313980280d0de3accc88233793dbebe28e545add4f742f9aa2c1a8ab`  
		Last Modified: Sat, 16 Dec 2023 01:52:14 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json
