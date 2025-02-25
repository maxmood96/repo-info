## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:cc3985464c35114136ce4ee23af932d1c66292bbf2f6385d4e119c25152a4ece
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e340fbddfbb2fa77a9a9e8ccd9bf452e1f13b6ae4bc4ae2ed2a66180a390c8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184192556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd6e546f79dc835656c96ee9501f637d464963052c5e462512bb5b14a13b291`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5715cf08eed2ec48fe1d1370fad6eb658563c0528f64dbeef58255e980314331`  
		Last Modified: Tue, 25 Feb 2025 02:15:15 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34387be61223da3ddb28bbaf4ff43f1da3e0953ab55419e1b07c432a2274d61c`  
		Last Modified: Tue, 25 Feb 2025 02:15:15 GMT  
		Size: 81.0 MB (80994576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1100aaa94a5c4e887e384224f89e8e36d9acfc6f8bc0344ae27a2039d3702`  
		Last Modified: Tue, 25 Feb 2025 02:15:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:322c5a6079f762cb148db918e6725d269a2720406a601851a8865b5633ef0aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db975616bda169999c0cc9e99dddc0e55d76b1f76e15a0031a8ed10257da3831`

```dockerfile
```

-	Layers:
	-	`sha256:83699ad9f2e2eaaa092b70070521c2281c8223dd87397c76df91b1d5a7db5158`  
		Last Modified: Tue, 25 Feb 2025 02:15:14 GMT  
		Size: 7.3 MB (7292706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b3f77eff6b030cec00bced06afd60542accb7e7385d30b5131833bc263e0033`  
		Last Modified: Tue, 25 Feb 2025 02:15:13 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b8766485b7ec3b66e50c9c0d0471e9f9301cae45bc5547c2403f246736530bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182975148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3327ad34409f45930db4bd290ef7e01c20993ae527f0349d2c5a33b97c98249e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9673169c1cbafc42d0bb7070c2d7ca116dfca5172ecd70bbc5f3f65919c5f13`  
		Last Modified: Tue, 25 Feb 2025 10:49:50 GMT  
		Size: 53.8 MB (53822778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae234104a43e0149bf3135edb917d1cc2f41092be956a610a860b91fe3a87f2`  
		Last Modified: Tue, 25 Feb 2025 10:53:03 GMT  
		Size: 80.8 MB (80843718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebefd38153bb8b7611ed0b63f4bd30041b828cc7a13711b26aa5ee843282ca8d`  
		Last Modified: Tue, 25 Feb 2025 10:52:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b35614711920f583de70d522cd30eeb4903eb0b8dc49d573421dfeaa36dee73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4c9dee4034cac7c418921eb225c9639ca1e7769d4170fcb4844091aa3faaf3`

```dockerfile
```

-	Layers:
	-	`sha256:ef57adb18e377ed0e6f983eddb05f134088a87c6c1c61bd371d79fc2c30f393b`  
		Last Modified: Tue, 25 Feb 2025 10:53:00 GMT  
		Size: 7.3 MB (7299167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b724ddb58f0108e9e842fa0a4463949675cb0184126dd22d9f5ffe40721c606c`  
		Last Modified: Tue, 25 Feb 2025 10:52:59 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
