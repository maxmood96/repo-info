## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:0f7919d12ccd44ca54d2e7685a34390f77b82120ea74304af96bdc982b649eb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9974e45a10e8345dabf8aa2afe1a0518ebde59b73d1d79daceedcf7278f037fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200500190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074cbff54f2274d8c5942e30c7ac38f133b7a27377c7119ff8e818e4cbaaad0e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83887a9377eaa4a06d229b4b7f2af3c23ecce03acbf79412afd4253541fd71f`  
		Last Modified: Wed, 05 Jun 2024 13:32:22 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7de49c4fd14cdbda45010cc16d511758a2a7d1f2c807f03c6bf61bc5a849e`  
		Last Modified: Wed, 05 Jun 2024 13:37:19 GMT  
		Size: 68.6 MB (68619639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34face56e4ea63908f28f7a87ab4c1ba30f7a9324667dc210fefd8d1fa102c31`  
		Last Modified: Wed, 05 Jun 2024 13:37:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a50712a69f7383aa91bcd7eaf128e9d9f14d77b3c4fcc8de9eab44ea8a4dfd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4748222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ca79c4319d86127365361beb36181c3104d4a0765e6422551a08dfb19e080d`

```dockerfile
```

-	Layers:
	-	`sha256:6557d9f26c20977a7841bea03eccf921be21f6e6f38971b8857efa5e14e4b3b1`  
		Last Modified: Wed, 05 Jun 2024 13:37:17 GMT  
		Size: 4.7 MB (4733811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc27792cd286b28ed550d8cd45beabb9bd7077277808f6edf2aecf049bcbf05`  
		Last Modified: Wed, 05 Jun 2024 13:37:16 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json
