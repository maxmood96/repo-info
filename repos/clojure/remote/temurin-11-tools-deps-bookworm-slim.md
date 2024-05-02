## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:74d47dc6534c3184179a51e43202c0198ae6131426bde66f15087b04f1d1ced7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b106a000df61af940e89b47055a63d02460afe239d88949efff2e69eb47241a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243722694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c285b1feb3e9fe0c59f57ba88fb4a098bf5f4c72481df7abccff316f280bf742`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:31:57 GMT
COPY dir:cf3bf634873a2f76d010dec9a72ea70ddc69381f0d8d3cb32fb43e16f4a2fabd in /opt/java/openjdk 
# Thu, 02 May 2024 05:31:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:34:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:34:39 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:34:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:34:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:34:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6999d802e184a3444400e20c51ed4b411a4c877911267d08e51549eb1da69ca1`  
		Last Modified: Thu, 02 May 2024 05:46:48 GMT  
		Size: 145.5 MB (145504632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a657a0368538ec8813ff68458a0d557d0c1b2307e59dc47f28d05fb519aff16`  
		Last Modified: Thu, 02 May 2024 05:48:27 GMT  
		Size: 69.1 MB (69066962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b79999b809001579255db947a666ad3a13d8e28617a2deada2fd84fa167002f`  
		Last Modified: Thu, 02 May 2024 05:48:19 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd29e51cbb23a3b8d2a25cf9f817d069e9bc88c9b4f1dbc530828164d197b118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240302587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e4feb614a564a017908a97e2b5740d563b6d5be1684e56a093a4bbcce6e611`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:30:18 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Thu, 02 May 2024 05:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:32:28 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:32:29 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:32:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:32:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:32:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0987a6f1fe0e0791144fed7d417846c016ee438e9987dc82e4c3e9513f7360`  
		Last Modified: Thu, 02 May 2024 05:42:28 GMT  
		Size: 142.3 MB (142304377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c43ae6cced1d06187856237204892b317ea6dd09eda7e0e7905c33b6a4e383`  
		Last Modified: Thu, 02 May 2024 05:43:57 GMT  
		Size: 68.8 MB (68817659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3422a0c927bdba4ead8154ada9adf115c50f7b36ccb4c608ae2533fe8ab18732`  
		Last Modified: Thu, 02 May 2024 05:43:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
