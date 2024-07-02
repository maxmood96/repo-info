## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:a6ab2f87f5e1bf2a2e6db21133e929b87d7d6aafc7f9451b2aef315b0701d2dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6077533aca47a2368947ce6511424d3c78d1d22a2faa2513343bf6ee7cc49b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193647218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff757b6c5cac8b2df19f895b2bbd622138f3025765b300c4e947a6b3311d587a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67239cc877a6101bf3fb1c13317b0c57107dd689de9789082b293e58071ee73c`  
		Last Modified: Tue, 02 Jul 2024 07:06:51 GMT  
		Size: 103.6 MB (103600228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2764c47d9548324b7f6b4365d4ad1d683e4768641067f46e77d6cd503d537f`  
		Last Modified: Tue, 02 Jul 2024 07:06:50 GMT  
		Size: 58.6 MB (58624062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5cf6b53f1e026cb419f627b72ab23954214321a00cdcb7cddf3ae24946807b`  
		Last Modified: Tue, 02 Jul 2024 07:06:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb5c8cb07a6c0548a63b3eaac660db8dd6db87c28a5692c0b962f26b4ced7afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2836dd95b562341f06da8c76d948ec8809215ca215e2f63ff21b69fa62026a26`

```dockerfile
```

-	Layers:
	-	`sha256:6747b84061a47480304fa71b23c09f731166ab769513e8880d02f82374e8eef2`  
		Last Modified: Tue, 02 Jul 2024 07:06:50 GMT  
		Size: 4.9 MB (4931760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9a5bf50e1a92d972da656108911c9a42fac60c005b67a91782dbb7f7daff03`  
		Last Modified: Tue, 02 Jul 2024 07:06:49 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:235c334773a46caeba60e193a92af7a924699fb307be8d6eac427896e9b2c3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191514590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7614bac390e4ac8eb47e9c254cfac73ba78dd4c9e171691e09ab3893205ed82`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
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
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d8e9c170aa38170adf1fa1dd66f79304a4c2c54d6f864079d077782e694d06`  
		Last Modified: Tue, 02 Jul 2024 09:13:26 GMT  
		Size: 102.7 MB (102700442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721da050d672be7453adc53b2d66eb51c5dfd1e267f484334c62dbd069d6d489`  
		Last Modified: Tue, 02 Jul 2024 09:17:24 GMT  
		Size: 58.7 MB (58743887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713abf0479eeef0fbcc7dc7b1f24d22b04a7ec3cd5528788d3829138fa861ab7`  
		Last Modified: Tue, 02 Jul 2024 09:17:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c8899d5a2f8d920ebf3a11cdd551ef29765c9ba9d32d6a0abea9c595902390c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4952576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc1c2d424880979b609179896881b661a4a4fbcd03d21ca0a7ba6aa33309556`

```dockerfile
```

-	Layers:
	-	`sha256:fe2351657f3241cd2be1b52fb3302ea26c6c15d75bda2ac6dbea62a304491654`  
		Last Modified: Tue, 02 Jul 2024 09:17:22 GMT  
		Size: 4.9 MB (4938116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5b96ea9bed1208f4cfa1ee97bc9e5026365e55904df18e8ce6f4c6931dffa4d`  
		Last Modified: Tue, 02 Jul 2024 09:17:22 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json
