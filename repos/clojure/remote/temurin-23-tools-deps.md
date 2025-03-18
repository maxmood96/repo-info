## `clojure:temurin-23-tools-deps`

```console
$ docker pull clojure@sha256:23e3166a1a9fa0224da3c1d4dd8a861c5a9e303aab43ea79085711938f5096bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:427202371bbbe8592ac981a07b2b370561ac6ad472fc52068ee844b2c0e2cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294786420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ed19d39b13e34fe2d7775e7312b3c60c29b6084dbe8a6f4f4a0855c597799d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b5ac0155384a97f60455cbf44b86f5e5d239ad69e4d543c98077ca21cad7b`  
		Last Modified: Mon, 10 Mar 2025 17:40:17 GMT  
		Size: 165.3 MB (165316229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b1eed4d7be1d0d9956cd24e9cebd64493cba7882e5ade59558f4adf85711f7`  
		Last Modified: Mon, 10 Mar 2025 17:40:17 GMT  
		Size: 81.0 MB (80993048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aca9ac7e25174a6be8ffd762547ecef99fad0968505eb5313b3ad83a63dd28e`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c6cb6a3f8b043c0879ba5987ae5e2ae0e9ff68b55a018740ca99f2cd67b066`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8babaf2f63f8d0d0c714d86385b02b80650136d98d15b0efd5a6863105cc13f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920941d19cc8be3703a3b97882b782023f171fae2683e664610029b001b210ab`

```dockerfile
```

-	Layers:
	-	`sha256:b7399b7833bc979a7282cd37db59441e413af7b2fa51b8a8c68afae457d6ce02`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 7.2 MB (7176785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a53fe06abc827e416750cabfd2c723427192fed02402b3f1560b6574710f2ad`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d1504b00ae2b8a63b2fde6a2d5c2961ae27ce0d284232c3dcc8426eafa095aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292489581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d1eba205423611b209a89400a52b17919efc4cbf66aaa3fadc327d5dacbe4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad9ee6b4c6e97f4c56459f18b4913e64ce06bc37df30ad27924127aeff6d0bf`  
		Last Modified: Mon, 17 Mar 2025 23:42:32 GMT  
		Size: 163.3 MB (163341415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f709858ef65b23c7d5737be38909e71fc58de81431ebb99cbc51b95ff715e1f7`  
		Last Modified: Mon, 17 Mar 2025 23:42:31 GMT  
		Size: 80.8 MB (80842269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaff36465c688e757368cd3fa82be1d99790b14a6bd58bac485b71ced1d31b49`  
		Last Modified: Mon, 17 Mar 2025 23:42:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c1ab1192c466194c927d77383d3c582d0f72f7ef2f32e1f74d4f85efb2dd5a`  
		Last Modified: Mon, 17 Mar 2025 23:42:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:b1cf31522e46940418cd0cb4fdfe8fd234ec4bedb80f5203b66e7f9562a2f1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9785d7a22858a702b1b72b0df3667f1fe32ea86d6c534f2e56859ff527db43`

```dockerfile
```

-	Layers:
	-	`sha256:8d666100a136008d1ecbb98d4fafe104d7676d34456b60ffa4ea7195543d7abc`  
		Last Modified: Mon, 17 Mar 2025 23:42:29 GMT  
		Size: 7.2 MB (7181963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c52bf9a650f73a7af69fc226a4fdbceebedcd30e9dfd00fa262b864cc810f6`  
		Last Modified: Mon, 17 Mar 2025 23:42:28 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
