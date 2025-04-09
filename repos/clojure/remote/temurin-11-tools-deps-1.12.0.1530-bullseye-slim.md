## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:64da11fe842d265eac23924084602e876ba6b9b56ad7bb39b3b3751a2ac74c1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b3d8900dbdc0ff912913316da39374468971b5ce662c2277b86bea46467ee414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234849704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa48bb1d1c8d80e0a11209905259bb9215347b17b099e2ba77299d14fe49545`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dc8a9d0985fff69a5b54fd0b694b5956f75112b8a28e3034deb14c18b317e3`  
		Last Modified: Wed, 09 Apr 2025 02:18:30 GMT  
		Size: 145.6 MB (145598787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34650f1180d25fcce400c88b21a2f4b558b8625f30c60288ad721a36d366f868`  
		Last Modified: Wed, 09 Apr 2025 02:18:29 GMT  
		Size: 59.0 MB (58992854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af63aff0b1ccd2a3c953098ceb4758bdbd220e0526aaf2f5a3213f1af90ae055`  
		Last Modified: Wed, 09 Apr 2025 02:18:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31a52e553dc5fc1cd9920e64312e2ad89afc756dc7e40bdc85fb29ad26217f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abc07472566c5b3135931efa71babc227c6389879f1e0744feffdba92e1d6e0`

```dockerfile
```

-	Layers:
	-	`sha256:beadce17662189efe072ae36f957fe8dd3858625e794ab7f3b3d565816543ade`  
		Last Modified: Wed, 09 Apr 2025 02:18:28 GMT  
		Size: 5.1 MB (5139154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2665ee481f116e8631a8561a4ceb3de6601b7e2d8ea5680392909c7cee8f47b5`  
		Last Modified: Wed, 09 Apr 2025 02:18:28 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b21945e09b0c7218a28437afa455201c63cb9e8443868bbba4aaaef0e5d74c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230263074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d3bd252e8c62d92031174071496b73d710ae4449428486149ee78b3035478a`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f86bfeaec95ef5ec2e11f38efc47425f6b274dcf46f09ceb8e0aa91d383d675`  
		Last Modified: Wed, 09 Apr 2025 15:20:58 GMT  
		Size: 142.4 MB (142385515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2935a0da88b222e9c5a7b683be01bd968d3fc8ff922103c7d254a7c829fec7`  
		Last Modified: Wed, 09 Apr 2025 17:27:07 GMT  
		Size: 59.1 MB (59127414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a6d7efae7d63d4b347b8f37689bc3dca401d7cd4565481df6b2bc2f58db92d`  
		Last Modified: Wed, 09 Apr 2025 17:27:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c14bf689fdbe9528fe97e4d02ae6d5ebca1addfc71f5246da8d4c0b429b83ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6ca030a93bf882de8b465b306c15ccf7b3e6749774c7af6d97afd6c1182b22`

```dockerfile
```

-	Layers:
	-	`sha256:50c612598615c1dd6dfcf0f118061ae98b90ec6db8cde1bc46fc66a3e702340b`  
		Last Modified: Wed, 09 Apr 2025 17:27:05 GMT  
		Size: 5.1 MB (5145504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d41614b446f940a321018beace93f3109d870eca7b30a5576075b9a3f5b348b`  
		Last Modified: Wed, 09 Apr 2025 17:27:05 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
