## `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:0d318b49647a395bf9868e865e24362b14a1d544aeda74b119525681b769a7ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:acda4f68b82bb6859a1383e7961e823ab9da205f17eedfb344be9d43545d6a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246763132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0a820c2f46c65745eca0adff53b3bff6ac929160b862a20f4ec6f02dffa111`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81e57942cdd041a3d96ef09857e092b54b3d393d46522445e839750ebac5596`  
		Last Modified: Tue, 02 Jul 2024 03:05:16 GMT  
		Size: 156.7 MB (156715499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57845f0bc2d6779a50033e5c0e3d9703595ae500a00904a50d5803422fb53e7c`  
		Last Modified: Tue, 02 Jul 2024 03:05:12 GMT  
		Size: 58.6 MB (58624310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c793c55560547541b5ad35a48ff4a461b0e39c04a2f21f82a6eb6c56e215b632`  
		Last Modified: Tue, 02 Jul 2024 03:05:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537cbd1f1952e0f4e41e4d09e9bb17ba30f6648515048861399f798b1184f728`  
		Last Modified: Tue, 02 Jul 2024 03:05:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4d64ea0211985065f9feec40d1f8600c6e43594c06d1f4ac3b9a0ab021beec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73aba37948fec4cce8d7130d6a32efa95c4047cbfa75fc3170760563ca3b5c7`

```dockerfile
```

-	Layers:
	-	`sha256:aa3e91e7641f6caeddcb6d3e3fe7fe92be0dad313749d9132366f5e54df75b54`  
		Last Modified: Tue, 02 Jul 2024 03:05:11 GMT  
		Size: 4.9 MB (4909266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12913e965f28285284381ca4ee7d86ccd03b8b74615419aeaa870eabc1065ac`  
		Last Modified: Tue, 02 Jul 2024 03:05:11 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acd1c7c9645103be0e19f1a4e250df8d6905b0a0e2b7fdfa4d017ee5e42f748e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243366144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5320829304cf3263e2d4d009e9a343fde366432e9e11331947eac6b56b7f9082`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e350b39c02b326f486ab2d8c055400ccba7ecc5d7dec7063c51b58e95ad06226`  
		Last Modified: Thu, 13 Jun 2024 12:02:23 GMT  
		Size: 154.7 MB (154738000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8fb91ce70e9339a3e64a29e743242388596c23c26399bb387b996f2d7b1782`  
		Last Modified: Thu, 13 Jun 2024 12:05:36 GMT  
		Size: 58.5 MB (58540125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cffdf07b10170981ce9d031b056a7c3be344d8261b5ebfa2d92a4593d864e70`  
		Last Modified: Thu, 13 Jun 2024 12:05:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477638b089c25d68ca76ff6e9749eeee41b0d5f8750e4919141ac748c8146584`  
		Last Modified: Thu, 13 Jun 2024 12:05:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e64be63612d7090bfc96ea8a0bad89294745822064e55c94c6eb559c42f702c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0374d2a7f282fd48cfa1d00ce6f55fea5d786cc07b3b85c7692b73b0d3ff0593`

```dockerfile
```

-	Layers:
	-	`sha256:b82f30be7cd70f1a2be7aa932537cd31f095f238e9de7ab37f43e21a141c1aec`  
		Last Modified: Thu, 13 Jun 2024 12:05:34 GMT  
		Size: 4.9 MB (4915583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae9187b7c0663f3a52ffb526077b4cc1b538f5e9b3df973864e82ae86a1ec57`  
		Last Modified: Thu, 13 Jun 2024 12:05:33 GMT  
		Size: 16.1 KB (16052 bytes)  
		MIME: application/vnd.in-toto+json
