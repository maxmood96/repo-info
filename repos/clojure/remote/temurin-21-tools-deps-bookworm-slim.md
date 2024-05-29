## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:fabf5632ec4151e799e5e81cb6905c97b979a17df169d9be5d06c1edb8941872
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8d900ce818493af0c772064501c3c4e0e6c9ddb9c015394f92e36e6be0108fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256517162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c64171a7f97acc9588aae9d07694c68594538c90e97adae6f996364918e86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24651d987a2e75e63964720e07e73969c555c53a3bb0772657a5f25cd5e5a1`  
		Last Modified: Wed, 29 May 2024 19:58:24 GMT  
		Size: 158.5 MB (158497991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007020339b8abfb0b0e98065e2f826a76b0dab5d4a30394350b9f49c210225c8`  
		Last Modified: Wed, 29 May 2024 19:58:23 GMT  
		Size: 68.9 MB (68867711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c1d057df6a16dfb669f06cf0f999722e9f0994a7e88ce1cacd3b30ef84f98d`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8c31fcf1f917f434043fde20b7226ec36807e916fe68e92fc74437125e05f4`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6976a25054223a83a757fa577230136f8cad62c0314148e8c9a6e97412d9bf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03b1c22e0665a76b5f1125da270f3e86fdfa3697950f4624e61fc3361c77a1e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4a12ace54260bff91859350e6cdc00fa8e52c47b1ed1cc0f932a14bdd5296e`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 4.7 MB (4705645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496d0215d46a7cb0b4c4a4d32c7d2a98c27e9e369e0d4c3d27617116b54922d2`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b89ae00a9cb76e1a94e557e8df653afa730f52c7f133db308db51a734398a1bb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254664535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3a2b8501185acc4198795b33c8390304fe118f0b32f9da714406415b106598`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:58:40 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Tue, 28 May 2024 19:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:00:33 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:00:33 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:00:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:00:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:00:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:00:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:00:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1920ac4105cbc22b81c26ddcaabfb2c362fe3c65503c90870b72f26ce9cc92`  
		Last Modified: Tue, 28 May 2024 20:18:30 GMT  
		Size: 156.7 MB (156665508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06828b245099f3a54f5945eb148ef3dc1cbc8a12b8995971bd1d4e4467c3ae3c`  
		Last Modified: Tue, 28 May 2024 20:20:13 GMT  
		Size: 68.8 MB (68818509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680c2b889b83acf5ca782d4d2c60cb6744e8d419d08e8e53b36d76f6221d78b1`  
		Last Modified: Tue, 28 May 2024 20:20:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4745fbcdf77976647496749cdd7406354e9aa339a2e0c18f71035fe538ddcf55`  
		Last Modified: Tue, 28 May 2024 20:20:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
