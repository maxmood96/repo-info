## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:8d579ba4fcd7354be2d82f4e679313cf02d4b1544065c75f166bab764cbea95f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9b2254b522c3a35847b708f6162c89e428b3de0f20bc2db5777e03696c2b3a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152473088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6980950865b7654442a9f84fd99ca1edd8d27bc840057d4b8325d88e10bf667e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030240ce91afa5acc5a765686455f19835f5f8a6c1531cf4302b9bb15b62cba9`  
		Last Modified: Tue, 03 Jun 2025 18:21:58 GMT  
		Size: 54.7 MB (54716183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679783b2a22299cbca9ce1045925a77dbd8d0d6b5acf5f3473216fc52699e2b`  
		Last Modified: Tue, 03 Jun 2025 18:21:59 GMT  
		Size: 69.5 MB (69530932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08deac548f3cf1b06982e58fa6d11d2af833ef02f13048e65e9398eb13ca8c2`  
		Last Modified: Tue, 03 Jun 2025 18:21:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f149457ba1bb3c95572b00b6122665fa65519e751406e8f2307822ebf56cc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba706a79ad61dba1d6b447d592094cad58d78da5224a9edec390c9ccadc5546`

```dockerfile
```

-	Layers:
	-	`sha256:784aa70bb2bca438deace330ca82d529bd72291f92fc97559479ca8349eefb54`  
		Last Modified: Tue, 03 Jun 2025 18:37:04 GMT  
		Size: 5.1 MB (5083108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194632867012480983eec78419a20fe40afb7c16f4556cfefca922e31574ad77`  
		Last Modified: Tue, 03 Jun 2025 18:37:05 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e6633b6a7104f8ee85172ed9606de4372f507817df48c2bc48470006bcafade5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151287931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5223c9d2c33400b5295d2f904ab976f4da4493ee772466496f49f5081535e368`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a417e3b74fbb7215b9587254b3c223d093abcb78011dfafa76141304d521fabe`  
		Last Modified: Tue, 03 Jun 2025 19:24:40 GMT  
		Size: 53.8 MB (53830503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb8c91442a9f3c21022b14d0a0a622aed90584b0747a33901eaab4bccb31a7`  
		Last Modified: Tue, 03 Jun 2025 18:26:13 GMT  
		Size: 69.4 MB (69391502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a5b4c583c2b74e851118a955506c67968b6285b42b386a240fe104ef46116a`  
		Last Modified: Tue, 03 Jun 2025 18:26:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d4737291eb3d3ef7a79132054d2fe002d9af897d8925f72b7eec5c9906f2bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3eaf84785f87083a0d41c44eb1cbd5a513abfcfcfa11f8c04f8b5b44feac7b0`

```dockerfile
```

-	Layers:
	-	`sha256:d3485b7c731caa08156d46939609d0b0c2485b238e6017ea10111a2e5d23de7f`  
		Last Modified: Tue, 03 Jun 2025 18:37:10 GMT  
		Size: 5.1 MB (5089567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:906e31156e99f59dcc441ae0085ea0603fbffc95b45b018cff06a9b6c8db0480`  
		Last Modified: Tue, 03 Jun 2025 18:37:11 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:166dc766a17b7b351f621f7998b7e5f08c0ae97d9d71c0518f02facd02c020de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159581563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3803ff4b6bedb89861fb4639bebf31ccb50cebefd50bcde9b55702b2a68b4777`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69330ccadd135120719a7f8e4da60763334e15c7b37c59d3bae3f4219bab28ff`  
		Last Modified: Tue, 03 Jun 2025 19:25:00 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f631dddc7696ce2297fcca3f933951e7c0d9c5ab6075ac47cd8524806371e`  
		Last Modified: Tue, 03 Jun 2025 18:30:52 GMT  
		Size: 75.3 MB (75346041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236256238be6cb2062f918ea57088995a1b2cf973f696d94c79e94fca1e44bb`  
		Last Modified: Tue, 03 Jun 2025 18:30:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f1c38aa3bf505ff7581374708d955e8f0dcc1049ef9c1aa2ce89c3fbeaad4ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed1f85c9c44a6a6e789207fcd6fbad7d144496d1763b6d5be9946c2dfe2bb5`

```dockerfile
```

-	Layers:
	-	`sha256:1d38c8686ab6d242cac4c26bc75bd59412fe4d5a8572d7a86220c424c0663ce4`  
		Last Modified: Tue, 03 Jun 2025 18:37:16 GMT  
		Size: 5.1 MB (5088859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbfbadc47ab038f0ec25e7cf3e09f6993794b8dbce9c9a7e3edf5570ee99a54`  
		Last Modified: Tue, 03 Jun 2025 18:37:17 GMT  
		Size: 14.3 KB (14338 bytes)  
		MIME: application/vnd.in-toto+json
