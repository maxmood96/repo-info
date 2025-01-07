## `clojure:temurin-23-tools-deps-1.12.0.1495`

```console
$ docker pull clojure@sha256:e8b21cf5c47e184f0b3561fe831a99b1cfcbf8fc175c98ee72058344ab58a69a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1495` - linux; amd64

```console
$ docker pull clojure@sha256:5c174a96a4bb6cb2ba5c74a9b8bbe3aa1e28794ef0356ff597ceb68af329965c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294569322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf22d5ff47ee49a24596e40006c2e5cdcf7423c379c00695bc258f707107bd82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a2b60981ecf3612b8fbf0a1e34e4be0efd56b143d6ee94ab7472cf96e1fed`  
		Size: 165.3 MB (165295113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c77ae1ab791110e038f5417b5de36ec66f0a46ea26cf9303e37193fba299f78`  
		Last Modified: Tue, 07 Jan 2025 02:29:37 GMT  
		Size: 80.8 MB (80776104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688e3a562f0684e14e1624be1aa6bfc1dcfeb8f496862ed3608935e719240df3`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea61bc28e84a83f7e6dd7255de52326d3b59779b863b5fe4d97f7d54161d5b11`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1495` - unknown; unknown

```console
$ docker pull clojure@sha256:b84fbdf79f0667c84f1a5b52ec6553921821415cb8c2c86632e626c58c8d0604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba9a5a69cb7657eb38aadcd621f01087a9082f4136b6a4bb9d775ea6db92fe1`

```dockerfile
```

-	Layers:
	-	`sha256:77691fbe916a3b8501515bea7278faa67fc08c6a2f94a538bff83536acf10191`  
		Size: 7.2 MB (7176769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9150547dd939b5ff5d53e3bae695dd9521685bb59c0818aac8aa28bb06c98f`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json
