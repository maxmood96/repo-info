## `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:ae91be426d977d4c325a1413f63c956d12d4bd3e992eacdf7398644b6592b8a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c52c6dd29b13891ba22c4a47b67902baf5d629d78e7ef496225ed28436586e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152630117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1838eba675648ae53cfc7b718cc88e4326b899a6b78d45174c7120ebba6aa509`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bedf44d1c376e2838c954836058cf3f229207ea12c44f37298b21fe5cb031a`  
		Last Modified: Mon, 15 Sep 2025 23:24:52 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a880e82bfbee36b718939e27aad6e98c0922c3fc06e54f58664510d95abc71b6`  
		Last Modified: Mon, 15 Sep 2025 23:24:50 GMT  
		Size: 69.7 MB (69669834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7453f14ddc6dd8234c4fc71b170a8a99e9e1f3d7835e91de133218cc24c79faf`  
		Last Modified: Mon, 15 Sep 2025 23:24:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3c1cb483706f7e403238e014af930e8147ce878eadfe5160a397fb6089001ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c40e213a1bfe8faab10fb8f1508dbf08b2850096d2055e1690cb65cf11d543`

```dockerfile
```

-	Layers:
	-	`sha256:e45ba9aa03da9e405db92df928db4b35523c05b1f621ddbc6c4b54a81c69244a`  
		Last Modified: Tue, 16 Sep 2025 00:47:39 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de33818e1f704c8cc34d323f35331b4b3c51959e44304d8739a5640741833b80`  
		Last Modified: Tue, 16 Sep 2025 00:47:40 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78585c4ca994e62a2f3be29a4750d3c1866b8db8657ffb2437cce026809f6107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151497657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a684c0ff4481660fdfa1fe3d48a0830ce550225196e3dae04ccd5068e65d9bd8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3b5a61b59e3eef5f4601bf1da0163bd35ead7cbe8e0e4cb145dd088478d217`  
		Last Modified: Mon, 15 Sep 2025 23:25:15 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b634beea3ed6a104d97f60d41b7ddd449f5a51d388557ddd65dded012ad1b7`  
		Last Modified: Mon, 15 Sep 2025 23:25:13 GMT  
		Size: 69.6 MB (69559307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2d2eccc3616a9f25d3401be35fa979513a6a604c38c613c43bc8200665bbe8`  
		Last Modified: Mon, 15 Sep 2025 23:25:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6bbc4831c0d89db0c84ff6b2670b1e703180bd711227200f836203e9f5a2bd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5941f493f8c1f919d1f88bba582b8ac0726df608199e70e3946b599558b7328`

```dockerfile
```

-	Layers:
	-	`sha256:bf2ce55f0105b60f4e403cf44612b642aceae79ee5923c9fbe684c688741de37`  
		Last Modified: Tue, 16 Sep 2025 00:47:46 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20cd510e4b39e07a72cfdf3af5fa453dccfc2d9acf8da8e86d91f5796e53a6e`  
		Last Modified: Tue, 16 Sep 2025 00:47:47 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:66f885b418751d7412e903d6ca2c590fdefb61ca97df19ea26dab0d010953a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159745586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21205a0e40aaef1e240d4564de765466da7b9c31d862d034faab7ac55eb544c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd1c7917822fb8da763ca8540975749cda2cc5d630f518864d2a00ff1bcc748`  
		Last Modified: Tue, 09 Sep 2025 08:51:00 GMT  
		Size: 52.2 MB (52165415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0040c45045a4a6fa2ec96aa998bd76e25f35914aa21ff97999b26a26df99a5`  
		Last Modified: Tue, 09 Sep 2025 08:57:48 GMT  
		Size: 75.5 MB (75510763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce705b3de506e416064d0aacf61642d052c5608e36ec20680092081b0e04bc`  
		Last Modified: Tue, 09 Sep 2025 09:13:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70f3783f28f1a4a49e97771513faf303beeb9b49923b71fbf81e411e4c6c3459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bce33fa715404b64449a11287748913b3c77b82b4cbaf6f953e7397823e5bb`

```dockerfile
```

-	Layers:
	-	`sha256:aa4b898a7de5e2de84d1d1cd59afe44007c87d554748177bf7c6c7bc2458e9e0`  
		Last Modified: Tue, 09 Sep 2025 09:37:16 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d001b4d051fbc3d394ec7da706e3bcbbcac67931febf20fd4d41bb3893de660`  
		Last Modified: Tue, 09 Sep 2025 09:37:17 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
