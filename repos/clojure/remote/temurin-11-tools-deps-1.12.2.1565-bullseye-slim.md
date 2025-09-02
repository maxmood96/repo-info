## `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim`

```console
$ docker pull clojure@sha256:6e544c0f0bcef3176c5996465590c29dc644963b04cf5884c54300c9759889ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:94f033f06c121d494a77c6fd3550828207fa76f22f40bbd30bcf698e86d6ee45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235065986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ffb1a44d3b3be3e3668c1a443c90feece6b8ace714db8ce26f09b454a6a843`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200214cb17be5ad368272bb20453e8bd357baaa308236355c2e4c82e68eac799`  
		Last Modified: Tue, 02 Sep 2025 00:17:17 GMT  
		Size: 145.7 MB (145658233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61d36dbc6d092f5e405fa8efbfa87596e2adf32cf3b9d35f5a3a06c0464b099`  
		Last Modified: Tue, 02 Sep 2025 00:17:58 GMT  
		Size: 59.2 MB (59150987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aeca62f696c591456e40ade00dae65a4d4a50c63b9bfa28b8da15b72cd6312`  
		Last Modified: Tue, 02 Sep 2025 00:17:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7eadcbeb0cdda7ae469ca1643d7d816611c969cc204005c67c1bd6d326dfd2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298fe12acbc7e874af5956a02d27de7e95df437d66c461d40b9aa499125d4fc7`

```dockerfile
```

-	Layers:
	-	`sha256:06c98b53c56fe08c7d40e9c9b74a85cad5e207a9df012aedde0545a458c9342c`  
		Last Modified: Tue, 02 Sep 2025 03:35:38 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab73b120c7c7e23db2a1a39265c8f053a75725fad0354d8addfb350be852bd27`  
		Last Modified: Tue, 02 Sep 2025 03:35:39 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5dfab2bbf802dfdb71017c854303119c4bf3957bc057ceee62ce2b2f1487bce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230494471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605447ba18af04428876b8747d74117f327330cd822f198f9481b2239020cdb7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3d476a7a6112e6c89c0b42631d80c8765bc27fb674cdd8928b9d51b6789623`  
		Last Modified: Mon, 18 Aug 2025 17:07:47 GMT  
		Size: 142.5 MB (142460572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5fe058dbfe69d7907eab2f72326ff68569b4c8d58ed51b74634ad747c6da28`  
		Last Modified: Tue, 26 Aug 2025 17:37:23 GMT  
		Size: 59.3 MB (59282761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0c85ff1ad06bf98e4a192057c2f81a217f58e9e8f787a4bceb939a3ecc559`  
		Last Modified: Tue, 26 Aug 2025 17:37:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff656c494953f4b02bc9fcd5c7610e8ee9f32e2da4bdaecb4a2639a2813a3c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6a64b5464b10bd3314a5d1ba2e06bccb06bc870e6753ee5e9eacc80d8cb984`

```dockerfile
```

-	Layers:
	-	`sha256:aa2fc8b52f377e92fc077d99814020946b13c578cdf013b5095130aff920fd19`  
		Last Modified: Tue, 26 Aug 2025 18:35:28 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d48d0a2aba116b214abcafc41183e8bc1c1565b2474566f2ac238185e32a642`  
		Last Modified: Tue, 26 Aug 2025 18:35:30 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
