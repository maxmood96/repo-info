## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:7d0f6e89c21962bf9925e2b298176ba56ef4e1f7cade9602bdff6a8119e290d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c42ae28ad45fd6a92b14fb805a119a15d68e4fdad7b2628c3da901da2dfaf426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246837162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2da9c191cd3b9a0ec56e4c4ba02ae5c9c05b4216730038fb587dc931d710a65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e67be89247749bc5c0185e0232df647cd7503eee17ace728c368a05a3a9490`  
		Last Modified: Wed, 09 Apr 2025 02:19:23 GMT  
		Size: 157.6 MB (157585895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6356d3d60eca8681d9eb90c235e4a321f11eee135d3fb163ad89cee3ba9de127`  
		Last Modified: Wed, 09 Apr 2025 02:19:21 GMT  
		Size: 59.0 MB (58992804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ca0133451a19a41582cf7246452a6cf58ba9de10820fc19515d32b4b07ffd1`  
		Last Modified: Wed, 09 Apr 2025 02:19:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e8c72e72214f5ed4e68f3d6d5895b713884968b89e1f30ea00204372d4e455`  
		Last Modified: Wed, 09 Apr 2025 02:19:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a1b23cebf258dec9f180bf38ade6d0d41ca10363340ac5140ce48eeea983d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816ebcf09dd326617b614eeb42e4d0165820fba930c5d3c70f30e4ebc3645760`

```dockerfile
```

-	Layers:
	-	`sha256:0a0d0a3b359955adb0d03e780123b72662d736aac012b0f847702ac49139b19e`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 5.1 MB (5122811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9452a6078e925674e44ee3e0b4014a0ffd848a6f9172ba3c1f874a8f844694b9`  
		Last Modified: Wed, 09 Apr 2025 02:19:19 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:466dab616dbb5c29c034b3dd70faa364714981ba8bd77b9b94ec959776e13dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243737119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780a5f0266cd756199a6de813340ced3b32df4fb1c1c7cbaced69ec5fc06421d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b36b65cac400eb4963af8b6530fb4d1fbacfba07ff7d990f32c967a8c0820ea`  
		Last Modified: Tue, 08 Apr 2025 06:28:57 GMT  
		Size: 155.9 MB (155859256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cede81b70520502e4cb546a631039e40b3a00cfd6945f370dd89cdac9c9bb27`  
		Last Modified: Tue, 08 Apr 2025 11:36:15 GMT  
		Size: 59.1 MB (59127323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c20faff078ebeac845dff30ea3b25691b031a9dc340040262c646796a50ca2`  
		Last Modified: Tue, 08 Apr 2025 11:36:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb50028bd221c5f05cc8adc08f1f0e1d154ffe385598f6d6ac6e70cd73bf32e1`  
		Last Modified: Tue, 08 Apr 2025 11:36:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42f28615b563f38abbf8bb96fc234c9e788d42e62bff0333aad1c10ecbed0286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ffd923bc2505c2594716dea56a4d0a65a2aa8f8ab639eef47c83598cb4a0ca`

```dockerfile
```

-	Layers:
	-	`sha256:d9275532bcd148c9688b16d6d83276257cb2f843ca93abbe1856e16e5e219c77`  
		Last Modified: Tue, 08 Apr 2025 11:36:13 GMT  
		Size: 5.1 MB (5128567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9040e5682110ab07688b4e605024db0fdd970867f32d54fd82350887e7da0ef`  
		Last Modified: Tue, 08 Apr 2025 11:36:13 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
