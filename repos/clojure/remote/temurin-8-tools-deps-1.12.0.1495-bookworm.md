## `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm`

```console
$ docker pull clojure@sha256:5a71e17542b46720e8fd8b5e57cab0ae438dfd192eb1aebf0b21919b001d5def
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9ec307ffd0abe7af37326888cf6cbda2b66d1902d2a56dc3afe9be9735003cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233092884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5473bcd6200db56ed65ea6b303bc1a9803d2e23b7b1dae16fe811c1c5ca3fddf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c032c85b01daca122a8053c2fd383b8257f36a67f10070d729019ee0ce34c67a`  
		Last Modified: Tue, 14 Jan 2025 02:43:28 GMT  
		Size: 103.6 MB (103633965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ddae3ae298271774595c0c051f986b65d61f8eb6edf19ee150e8eb37598fdd`  
		Last Modified: Tue, 14 Jan 2025 02:43:27 GMT  
		Size: 81.0 MB (80978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6eb5ac73d4758f6647002271aa7a0a30d91f4af8fc1efe7b64a43553009cbd`  
		Last Modified: Tue, 14 Jan 2025 02:43:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c29a5aba4b78b29a85b76fde9fa8d3ff28b38af8484ce69ab8f5a4060eb1823f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7307539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b19439dff2cf9285a0932d437c70d363893660ef8e14ac8aedd2e1e9b72515`

```dockerfile
```

-	Layers:
	-	`sha256:32651110f26354fd5e54834f1a6085b001f76ad8f8f2e3b46550d227a5c87751`  
		Last Modified: Tue, 14 Jan 2025 02:43:26 GMT  
		Size: 7.3 MB (7293298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c816f87ab7c28ad7f57878cc0e8c25c0830eb55a802a5b4fa99981b3ceed30`  
		Last Modified: Tue, 14 Jan 2025 02:43:26 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:63828dd6c8d99d355cf9068bbf27379cd2963200006b03a1c1e0394bbb84cd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231697674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ac8838c5c0d8ea27b0241bfb5dd5c610f10ebbd017746c554a1b4edbf17bc7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112fd3c245deeaab14c956138bcb866289ea45497d0687528ac34f2dd5bd159b`  
		Last Modified: Wed, 25 Dec 2024 07:11:16 GMT  
		Size: 102.7 MB (102747746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3170a46c4357683b1b2ab927a408e8429735dc487eaacc72fbd42d29e01f63b6`  
		Last Modified: Tue, 07 Jan 2025 03:16:39 GMT  
		Size: 80.6 MB (80623801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9f87b585809706275a5bd6c13ec6f0dc87356da7646328db29532c0868214d`  
		Last Modified: Tue, 07 Jan 2025 03:16:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:75bb2f99fc625920062d86eee039a2f6d307a8b9c1ee8f3eac2c5cbc3cc303f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7314119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fba3a4f838b4c8311a68f51c93cff9b1b62ad415030092b5283d1b4d7631f9b`

```dockerfile
```

-	Layers:
	-	`sha256:ba0fd0f23d4426d9bce9e1ca0a71805aa548d60f75c0fb691ba11a0f3d0eaa95`  
		Last Modified: Tue, 07 Jan 2025 03:16:37 GMT  
		Size: 7.3 MB (7299759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6aa6534101689abca7728dc68361502648f4b920c40fde276b990415dedf2e2`  
		Last Modified: Tue, 07 Jan 2025 03:16:36 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
