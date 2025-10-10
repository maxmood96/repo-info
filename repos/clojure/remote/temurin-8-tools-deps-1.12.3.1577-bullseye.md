## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:c154b9f81fea3ccbb82c29f2a229c18dad12ee2561af2846f8174217ce750b0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2bcefd4fa2de49d319de3e83f8769d64f4373de6365ba1fd4a129dfe74f2ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178048698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0cb39eb045b23d14a4aa100991327cfe610153309bae25dfbfdce8cde8a4f7`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c7042aab1c60d564075fd94085f41669fcb81831b12d4c175b4c995298b7f9`  
		Last Modified: Fri, 10 Oct 2025 11:27:18 GMT  
		Size: 54.7 MB (54731352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35f180ec6fa8ad77b9756cc9b02f8edcca327cb03024dc2fcd14dfa7b354cba`  
		Last Modified: Thu, 09 Oct 2025 22:26:37 GMT  
		Size: 69.6 MB (69560637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb91f3ab16b6544679ca4f70ceaa957f15ff35f06d917f897985b4b5fe0b55a`  
		Last Modified: Thu, 09 Oct 2025 22:26:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b0fc1f49466cad8c5bdf66bb672dbd10e2f99ff434a449211defadad1700b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7533138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922dbaf5093e21eeff56e3c2ff8097b753ee3b83fb3e864c40d5dbe78df1b908`

```dockerfile
```

-	Layers:
	-	`sha256:7545a89ecda536b750ebd015e1eb19b66a91069865f14ef6fb7e4a5dfe815e64`  
		Last Modified: Fri, 10 Oct 2025 06:50:14 GMT  
		Size: 7.5 MB (7518901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7caecd3d6f796465345cf859cc7ae9222ce3ba6fb53c7d948ad349e86f5a281`  
		Last Modified: Fri, 10 Oct 2025 06:50:15 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:489fe973822cb339a39a5684c164c71c06231be43ebab7eaa2bc774f8e2e36bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175781687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96492a4f758d622c0a8e817a5ab64f58cfac75dc4694055c70586a41d61a65`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553091cabe41dad4989f6ab8dbceb94014614c8d01c989fa974af47a32e3f87b`  
		Last Modified: Thu, 09 Oct 2025 22:26:40 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d4ac032233d97365a779c1ebf266104b0f8bb4909110a67cf15acadb25bbf`  
		Last Modified: Thu, 09 Oct 2025 22:26:33 GMT  
		Size: 69.7 MB (69688022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33983e0c699462fcfe6c8f04ee531ea8458e3c25e972b7452fcd4ec68792b1`  
		Last Modified: Thu, 09 Oct 2025 22:26:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bd406fa13c3ccf2b71816d254dfbc0206b2a50afe694fd32107ae643fbda7025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7539053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb331fa33c24ffad6c77be5d317d9caaa52af3d2ad6657752ad77fd0cb2feb72`

```dockerfile
```

-	Layers:
	-	`sha256:6256ad7bca26f34d7b54502ffb58df857d25a91216c4635aacf1ad0daa1ffb62`  
		Last Modified: Fri, 10 Oct 2025 06:50:21 GMT  
		Size: 7.5 MB (7524698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a7cc6369e897d3098d88143db31eb24e1d2011b98dfae3e52d2c5055dd1c2a3`  
		Last Modified: Fri, 10 Oct 2025 06:50:22 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
