## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c1b7d49c5d8269df5259fc0b995c12bf2f3bff221ee7f112704c2f607cc6ca31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1f25c5f39d0eda372f91d9bdd578b67db5f30786aee41245c74f78597b3f9671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227516808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2040e4c8f477929396d9b367d0f36bd7be7eeeb927d968423ee6feecec49d1e2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855293a30b8c9632aaec07f0007096f08f0b6dd5072ee7ed052a6c282e5e7768`  
		Last Modified: Wed, 29 May 2024 19:57:08 GMT  
		Size: 103.6 MB (103600211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b279bc467579e30a06e7e84f05481844976218fa30d397dd2da8633b3d630722`  
		Last Modified: Wed, 29 May 2024 19:57:08 GMT  
		Size: 68.8 MB (68816551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9a0d281ba2b40b2ea55ac5f0a1826debf3c19b9a0d5bbf3fe19a75894835f8`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:abb2b91a5a1d04f8da09a7e0e5f892db083f10827d7e56d1bc34a7e4dbcec5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243652c3455d7d930cf04c1ac900d6362d0172fc5da752051b4b8b0fe3d065db`

```dockerfile
```

-	Layers:
	-	`sha256:1b1c976ec5d97353376d526ede0efc3b51aee1d1b8a45aaaff1e8268cb45cbde`  
		Last Modified: Wed, 29 May 2024 19:57:06 GMT  
		Size: 7.0 MB (7022240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732a05c98f1b433b54409fa8dbdf9ab087e1b9920481598f1696d467f7de598b`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75de33cbbc99c69e908da8ffca7ab839be3a6725e72616608bf790ba17f4ef1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225369241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a8e0cf1b9294879f1707edf05b0c891d73953ddcbcebab13ab73fb754bf3d4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
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
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63911e15f438f0df584fead0a70409ce33f1ce399ac96a51f4a8a5525258392a`  
		Last Modified: Wed, 29 May 2024 20:26:37 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bdd29ea98284b1d4f879ffbbf2ee029a7c102605a6460ba79b65d214c0d3d4`  
		Last Modified: Wed, 29 May 2024 20:32:17 GMT  
		Size: 68.9 MB (68929207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9e62768cf822f3f767038ccded36bcf677cc42bd20b71c352ae97613086de0`  
		Last Modified: Wed, 29 May 2024 20:32:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a2b608e3116fc2e059b6e78c1ab112119de66e43111b0994460cfd8d4137f6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7bb1cc18aea783f324d67fcb5bae07e5b6a84d2b78c5b54cf108af22dc86fa`

```dockerfile
```

-	Layers:
	-	`sha256:88e2fbff17fa12d76fb14ff3e3076e3d4b11ccdc253ef71dd7f6736d90c3798b`  
		Last Modified: Wed, 29 May 2024 20:32:16 GMT  
		Size: 7.0 MB (7027962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b627d46d039edb882302042045606f10f5704b13796f09cdc01ad6851f55a108`  
		Last Modified: Wed, 29 May 2024 20:32:14 GMT  
		Size: 14.3 KB (14337 bytes)  
		MIME: application/vnd.in-toto+json
