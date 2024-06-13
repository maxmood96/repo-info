## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:8beef91e6962520a37cba288c432328f6ad0b8b65f39c15a04954d46706615f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:00d671443f9c06450a716991d3c8b21672ba898c772478429864d3403043df60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201619814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df790ad7bd57335ddd04f5645512fa6363e0df0f2d13b725d444690aaeddb193`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30257be913c05164f0ca7eb4d07bd3d776fce328a3f0a3c2494d673de9d4eac`  
		Last Modified: Wed, 05 Jun 2024 06:09:59 GMT  
		Size: 103.6 MB (103600188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef3a43c906ca2387644ba10055f5fff7c167ca8071268406ad2310c24e7f623`  
		Last Modified: Wed, 05 Jun 2024 06:09:59 GMT  
		Size: 68.9 MB (68868567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cdd5088e027e11cdf277c220995c2226273887005a73d65ea56afc19d43a2a`  
		Last Modified: Wed, 05 Jun 2024 06:09:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd6eb09307d9623aa15f6ad78055b81974193a844e7b30e5e08527a932da3b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4741297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b38cfa1420e8d2fb5360237f729fb28902dfb02464586800095f20dee3ef26f`

```dockerfile
```

-	Layers:
	-	`sha256:8c74cdb38f84225020ff8ef52e51a7cea15e5ac3d0defde9cb121054b2d59389`  
		Last Modified: Wed, 05 Jun 2024 06:09:58 GMT  
		Size: 4.7 MB (4727426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f9656980b79ed176124c9dbf6b9c3ae4f8e60a4ec0016eebc1842d3d51c8518`  
		Last Modified: Wed, 05 Jun 2024 06:09:58 GMT  
		Size: 13.9 KB (13871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d3f3b0e42f044fa2d05df85fcd8cb494d6beef6b5d3da72d2401eee9704f08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200501208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507a3233f6477684d7df13264a9313b45461f623b54712cbe53e26110a65365a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab2e61ffd9a81e8a8962bd8afec8741dfdf92978bd880ae8228d1fb558eca13`  
		Last Modified: Thu, 13 Jun 2024 11:21:17 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2605297d0c66832f95c152dacedef5f44e01743fe01f126c6f95e516384fd2d6`  
		Last Modified: Thu, 13 Jun 2024 11:25:47 GMT  
		Size: 68.6 MB (68620493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7492410e516c81137a2ef783385c26bf87d8dcbc327dcfd40539839eb8aa31f3`  
		Last Modified: Thu, 13 Jun 2024 11:25:44 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb7fe2302bb08654b7730d53cde283be376ee75b32b0613bd87c47fb0491b6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4748271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f843da8a682b3d0498a3b436871982f67b47528cc130d9c8479c649003156470`

```dockerfile
```

-	Layers:
	-	`sha256:c809a5a1d29cfb967a92b0b54af3d76ac8bcd0291d445f6cdc8a5cd16f3baf4e`  
		Last Modified: Thu, 13 Jun 2024 11:25:45 GMT  
		Size: 4.7 MB (4733811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b861b9e5181cf0bec969117193b45401b12398823a3b0a65bcd58dc296e94af8`  
		Last Modified: Thu, 13 Jun 2024 11:25:44 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json
