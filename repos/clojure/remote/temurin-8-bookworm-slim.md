## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:6e204b168c34505b15ef29820b5bf7d0453222af2081ede7f80cb9353f27e55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff8da1f2b0ed46439045223500759732b3faec12bea8a73af6db4265131705aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201817826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9616c1efc22cd050ce309439d3ae4d6539a32f471d20dcc64f68afad64c04e0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:21:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:21:35 GMT
COPY dir:54f5f76f9b290ecbafc047cf196165b69f1cb32e49c8748c35e250f5e316fcc0 in /opt/java/openjdk 
# Tue, 28 May 2024 21:21:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:24:24 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:24:24 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:24:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:24:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:24:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3575c8a15ff96c0b65edfb87ea49d12f54ef159c0d1127db78dbba966ca33844`  
		Last Modified: Tue, 28 May 2024 21:49:30 GMT  
		Size: 103.6 MB (103600144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf76c41bd27e9e325178fd7e5fe49dd166e352cf06abd78b8ef2767f5be57cd`  
		Last Modified: Tue, 28 May 2024 21:51:14 GMT  
		Size: 69.1 MB (69066655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c08889cd642ddd7c1667d853d910f236450ad0c314583a905c3bd7c5704502a`  
		Last Modified: Tue, 28 May 2024 21:51:06 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0379784352057bcc8507853056e6353cb2c359a20f2edcf56f5b480836ea47d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200698351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd149dc3eb183bb91d6214433ac2408e513cad018f1b5d33b652dad5e35eb3c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:44:30 GMT
COPY dir:f816a852ac21a5e29532918ac40e44b27f618ca8c5c539e334f114f460fe4b51 in /opt/java/openjdk 
# Tue, 28 May 2024 19:44:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:47:34 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:47:34 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:47:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:47:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:47:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389a7c333db397c8ff25702268dd937ecab8cbf425702f761dc333c1c7e9cd21`  
		Last Modified: Tue, 28 May 2024 20:07:57 GMT  
		Size: 102.7 MB (102700147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aaac27087aed625373b7b6d12b5183ba35198e8cd10b9c5a1eee2561057f0a`  
		Last Modified: Tue, 28 May 2024 20:09:34 GMT  
		Size: 68.8 MB (68818083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e6965d25e7fe1739cfe7a5d121618bda7237bfd752c3b5ee8c7a4aec624a9`  
		Last Modified: Tue, 28 May 2024 20:09:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
