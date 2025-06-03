## `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:4766e981625c28b043279f8c0f2e6f7ff042e1a4f5a1e1080fcd9bb4d6494a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4d06a7c35ffb1ff8ba1c8da7c699fd36257771c7b0d226c047c68ee8a683379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143966855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715b5ecca4c4a3e71744b0ab5c8ffae1675a5ee9ee18135da6cf186764087126`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903cd755cffc34ca73762e36994a0e64c1300a5fff34da8aa47ec6d208858465`  
		Last Modified: Tue, 03 Jun 2025 05:15:22 GMT  
		Size: 54.7 MB (54716179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad5bcfa92e8a363e721a2aa2ea8bf5c0eac43eda8e5414dc3a7c0f8db629e96`  
		Last Modified: Tue, 03 Jun 2025 05:15:23 GMT  
		Size: 59.0 MB (58994091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4e35df37660a10563ff471cf05b03702e7f9217dbebfba8a84d5e87842a37`  
		Last Modified: Tue, 03 Jun 2025 05:15:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:907eac6d4d8501c5df35bdd7b2b53c1c631261ddc7798c69563c7cdfd01bdbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f30a020397f9d977b0fa82a4e2324225ca24d0ec1a3da97a3a6161ec6540cdc`

```dockerfile
```

-	Layers:
	-	`sha256:4304f960ce34526a8c89ce34a2592e0e6cb87222758db0fd2333e0366d25cfbc`  
		Last Modified: Tue, 03 Jun 2025 05:15:22 GMT  
		Size: 5.3 MB (5290196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b718bc66edf4306154c73a7cbcbd5333df26288283e96f7f9a307d7caecc0ea`  
		Last Modified: Tue, 03 Jun 2025 05:15:22 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b34295cade83de82d3fc0d440e30cfe220f74215d0062bf14ef91711b8e1bb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141706277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f72914b415d579a7fef054bc21b7fb4f07107fffc36a05bc809529a903a4e20`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a26ea748e01f6fa271cb5c99f02841ad6f2c475c5d2be97781534dee920e77`  
		Last Modified: Tue, 03 Jun 2025 10:29:58 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82f92517909d578477a9f7b73af3f5e4e7a6ba48c5182e81efca5c7eac231c3`  
		Last Modified: Tue, 03 Jun 2025 10:36:11 GMT  
		Size: 59.1 MB (59128878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada409887af2e62dd91570adc18c06fdf0ad3dd149c358b33824f8f02ad72ee9`  
		Last Modified: Tue, 03 Jun 2025 10:36:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a6669adbebedc9c0589374309cfa6f449f5514c52f478df390e41aad0b1ced5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc32047dd32f5a47559dab0ebaa31ea0b4661b6096c97f6e305b49952c89e403`

```dockerfile
```

-	Layers:
	-	`sha256:646236e6c470d0833ef63e0367e37142dc48e20a76d227aa5e01adcf5c8c0226`  
		Last Modified: Tue, 03 Jun 2025 10:36:09 GMT  
		Size: 5.3 MB (5296626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba8d5f5a7126d0d982edaf886b0002a0abbfa4b0b67a7f521db79a26534da52`  
		Last Modified: Tue, 03 Jun 2025 10:36:09 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
