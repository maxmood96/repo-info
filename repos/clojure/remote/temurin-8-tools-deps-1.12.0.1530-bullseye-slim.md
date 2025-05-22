## `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:b89adb82d5f6150e360b2a6aef6da282288973f53a0c2c19a716ecea44079450
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7e47ccb43f9e3d98816c46bb01bd33f3cc792a9cd5e100ab60de4f3367f4a9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143966743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906180469cd908e551d00d368352ecc0f08d86126efa6bfc5e484b3cca84422c`
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
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbe380a355495bc5e38d6d1e3e5fec428c3fd1273c709246bd8ce0d0fe64254`  
		Last Modified: Wed, 21 May 2025 23:31:54 GMT  
		Size: 54.7 MB (54716171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786df985e83238a21611bd54d4945ce34614be77183910f49549af67930ab940`  
		Last Modified: Wed, 21 May 2025 23:31:54 GMT  
		Size: 59.0 MB (58993988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137049063f3183a0773f866481facfd67ce0c1b01be4a10fa42683dc0a031929`  
		Last Modified: Wed, 21 May 2025 23:31:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3add01800cda1ff37e4987807ff874fbaccf5c121edaaf5870d716f1c93f1fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5302891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a832c9016bdb134373e05e8df52efd6fbe7de9727f5f06dc6e418c1e6e5f08ad`

```dockerfile
```

-	Layers:
	-	`sha256:8d79f112c6144f70bd185824daec86f8ef876b74394d942832d9b6fc67f27022`  
		Last Modified: Wed, 21 May 2025 23:31:53 GMT  
		Size: 5.3 MB (5288600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae5ec3172aea3fea7276a64c6d1d9739f28a651587df381f53c05fbd576cef7`  
		Last Modified: Wed, 21 May 2025 23:31:53 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:921b96c52ec7168ed42522fd9fc664cc89fc11c1a455c5d532ed877209bb2c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141703192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc443022b1f88c0c80f03719a0998507886ff2d2cc93166ba0aee58176ead6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9362c53d1c14ecfefba9cf38dd0fa524f1f96fc993f360367b03a91b556103f`  
		Last Modified: Wed, 30 Apr 2025 01:00:56 GMT  
		Size: 53.8 MB (53830503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8d67647b92f1f5f5dd98c61327d4113d300f34a9f4dd2555843c503eb3aae9`  
		Last Modified: Wed, 30 Apr 2025 01:03:37 GMT  
		Size: 59.1 MB (59127402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc57bf9dc32ce128463041f93704e685c08353465d76eb509d6c9eee0daa51bc`  
		Last Modified: Wed, 30 Apr 2025 01:03:35 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43ecab4f80d55c30ae7ea1cae4b7dd2881cbb16de63582bada4821781bf4bf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1376c9ae089941638cc9932cf36d9760a6fca5e5675f8464a8d2d466d487d1`

```dockerfile
```

-	Layers:
	-	`sha256:0db8f95576ac1eba2ac94daea747521a8bb11eff4291187b111a952de254cc40`  
		Last Modified: Tue, 06 May 2025 00:20:58 GMT  
		Size: 5.2 MB (5247107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e89efecc712bce757acf4938bf230e5a7de31547650e1075f422d501429517`  
		Last Modified: Tue, 06 May 2025 00:20:58 GMT  
		Size: 14.4 KB (14408 bytes)  
		MIME: application/vnd.in-toto+json
