## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:af04ee96b24e4fbbccd19bd471189e105d4f08f923d5f07b4c1b58c36ad7037c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:998e603562b55222c2ac3eb4c3a5560341a0d56ba5f152cc9b28f0bfcd5e1a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179203156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ce3510c6cd0c9bfbbd7f6a87ae720acf6d91ccb8f88794c7df1a53a21cbc47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bed9dd916e9f117d9ace8cd7485f83376b5ef7ea0cca34281e626b44cbff003`  
		Last Modified: Tue, 03 Jun 2025 05:16:52 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3058aa72aab5ed712318b36bf857dbb620aacb00e3ccde25eeb7e9254f807c`  
		Last Modified: Tue, 03 Jun 2025 05:16:51 GMT  
		Size: 59.0 MB (58994157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c9b12aac89f03f865b2b8a99c39a379b57c3e325d752f61c1d95ec9bdd5808`  
		Last Modified: Tue, 03 Jun 2025 05:16:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78588f7605e8d8090ec9ff67252579deb2b06df39a329adae368da573609239f`  
		Last Modified: Tue, 03 Jun 2025 05:16:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c25a527db491723b3e3ea592fabd60f9b776fe0bc07345cd4fafe00fb7ae83f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6351d58e1033f23f6c6f925c291da5c55a9a9b7f0e02de6143c6ae40e2157734`

```dockerfile
```

-	Layers:
	-	`sha256:4f2e22e872e1b1647b1b53e015990c8a162f663b4a507cc34175aae8d1e28b57`  
		Last Modified: Tue, 03 Jun 2025 05:16:51 GMT  
		Size: 5.1 MB (5119232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcabd9fe914df79b0fc87050b0a10cba32f76ba917d4ed740a519b7405c86683`  
		Last Modified: Tue, 03 Jun 2025 05:16:51 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b11c57e14819a0a489400ce4db24700943a31f1a5775114e5bea3266cc4c6f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176967526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d0199e39344c8a4d8f271be6dbbf3d8175612760425c2f290e9699fed02072`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bded46ee81e89e59e64c533c353440bea9d4be7e5e0f2def77398507b60fd0f`  
		Last Modified: Tue, 03 Jun 2025 11:07:45 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb6f7103b4a09a26263902f9ea747480fb920f7100aa3154b00774c9b91bdda`  
		Last Modified: Tue, 03 Jun 2025 11:13:17 GMT  
		Size: 59.1 MB (59128956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7328ad723400e3fa758723366ed10747a1fdaf1a9f0fff833e9045151a2cf45b`  
		Last Modified: Tue, 03 Jun 2025 11:13:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a98af198477f1f605563b285c3f206e2d3c806fb540da3492e2a965016b3d`  
		Last Modified: Tue, 03 Jun 2025 11:13:14 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0b483d53103a1e611fb630a465b2b255052ec7699f11fde331713d0f40f763f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb63b7779ecb6de88a097c660b553c4ebef08775e78f536a8278c4a05ac2e4e`

```dockerfile
```

-	Layers:
	-	`sha256:f4520b861f9c2712b1576639b1dde0c4aaed078be65c4d9f7dda8a2a504e8136`  
		Last Modified: Tue, 03 Jun 2025 11:13:15 GMT  
		Size: 5.1 MB (5124961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2fbd59a46e3f1d67bcd0f67918ac063d210740319c394487d3d43b26d1468aa`  
		Last Modified: Tue, 03 Jun 2025 11:13:14 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
