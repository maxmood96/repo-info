## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:9897acaf524c531ffaaa115a47bfa0c10534a048a377cc7f7bd71324a56a7765
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:950471438ffc4d359deed5ad9feb90e929894dd0bb11dfd1d93156975d1eb731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268532011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e895f13b6181cbff001e2f5ab667908c5bd2d99532f39f0e6aa8e56ed06003`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebdb53a89d9470b1d6698783c75eeb474fe3b86f64f6d8528b4588b91ce2f97`  
		Last Modified: Wed, 29 Jan 2025 20:27:30 GMT  
		Size: 145.6 MB (145601445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0676e6c16d7076a24f80bdce0fca6f7c5e584593620a135a5e07e4d07c5233e`  
		Last Modified: Wed, 29 Jan 2025 20:27:29 GMT  
		Size: 69.2 MB (69190759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7bae4b7eebe08f0cf628d94788c54423b2319e71c0ec6375235d007b1c92c0`  
		Last Modified: Wed, 29 Jan 2025 20:27:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3c365dda8cfacc09144d459797e62d30fe02faef54727ce94b4faa1fb7f4c498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fdf91d15b3eacc9c1096f7bbf548a17d40b6cdb641801caac5a3018659f734`

```dockerfile
```

-	Layers:
	-	`sha256:dc423d92fc75d4375b551690e58383096cb72bc88c90d671d2a645c034b15e88`  
		Last Modified: Wed, 29 Jan 2025 20:27:28 GMT  
		Size: 7.2 MB (7224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5ae074b45acbca77ea9c10a56dbf2d97b73a33a298d4d8c65cfb6116fffa40`  
		Last Modified: Wed, 29 Jan 2025 20:27:28 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c267c7b66f6e092c844a7d7455db6da173047b66680555e708b4e36bc3e05bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263947670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dd5d22c5c637f1bc60e663d3057434bb7f2c13f4b730d701902593812f5f75`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9dc487771b4c51de1db706de22f9c866cb24d1d041206a8329d097bb833e43`  
		Last Modified: Thu, 23 Jan 2025 02:36:37 GMT  
		Size: 142.4 MB (142389512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec323f59422a9135ec1c105c00989de73a52c2e77da76ff24568516fa3c9f1`  
		Last Modified: Wed, 29 Jan 2025 20:45:08 GMT  
		Size: 69.3 MB (69311454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117b1015c889dd4ca8c5604fe2aec6f52a84a00a3609b5f74f4382f2879128a`  
		Last Modified: Wed, 29 Jan 2025 20:45:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2d840c945a6bc77677cde5a2767c4b9b3731b930898b20ae6ba756f4c0687661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7244783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817b2532d816108d956d1f0d7bbcdf4d590623126cf2d73f1838aa805f684ecf`

```dockerfile
```

-	Layers:
	-	`sha256:166e964d4a59b87bdf44b00732ee20fb961123d34d765bbae2c13116d5fab95b`  
		Last Modified: Wed, 29 Jan 2025 20:45:06 GMT  
		Size: 7.2 MB (7230413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cb680581853e915e9fe75b705646d8a33024ca838e7f1ef13eac2abf498d96`  
		Last Modified: Wed, 29 Jan 2025 20:45:06 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
