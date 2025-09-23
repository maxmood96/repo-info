## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:5efc54852217dbc4c63f9755b6d5f8e014f602c03f9f3b9edf0bf7e60aa9cb9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f53545ea7a502b91c0359a2c079e0182e146c16ac0e6d15e73b81fdb692d2c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243562395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c6d1ecc0da1d93f9206a1325ee38478708274564c7f6be2e0f72d444c75681`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be3ee7f4183d6e7c998c8f0debafb60ef06614f4e88d341d3f884a42040e4df`  
		Last Modified: Tue, 23 Sep 2025 01:40:24 GMT  
		Size: 145.7 MB (145658246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff50007f3f066c28bb73be832b8f8a1e2f96eb078d4b42f30a04e3379f214a7`  
		Last Modified: Mon, 22 Sep 2025 23:45:02 GMT  
		Size: 69.7 MB (69675156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6ab2d2d311081ccb8a75bfa9ae4d0421195e5a3a2892f5391a1672344dafa5`  
		Last Modified: Mon, 22 Sep 2025 23:44:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b3c5cbd20d82961e7aa8e5bee955e07941f69c62b4f4c9fad922e9ba740dc6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf91b328575f562beecac9cc838b535eb0e469848de1cbff5c59c046a7ece3`

```dockerfile
```

-	Layers:
	-	`sha256:7e78c46aed13440a73290856c1089c25d88fecbb423b4ec8bf277f4e97c7406d`  
		Last Modified: Tue, 23 Sep 2025 00:35:09 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b80ef695c28c578e5e826d9ceb9f00749f4f7a815373063ab39a1ac00cad63`  
		Last Modified: Tue, 23 Sep 2025 00:35:10 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:67422eb1b67973e38080d6aed2509e3994aa8e3f067ad0f63bc382b3056712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240125274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0166f611f51b21228bf6df7decfb0f299d0b255e08d35df4d81bd8fd672cf6a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6df4e5825a464c08e2ebc9667b0d94a8f6a11f888ac788353709d9393b415a`  
		Last Modified: Mon, 22 Sep 2025 22:17:07 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd568e884c4b5c24f692ca0e47bc4c4f504673c2872b66d04ae944bce4e11a3`  
		Last Modified: Mon, 22 Sep 2025 22:17:06 GMT  
		Size: 69.6 MB (69563772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08cd948a5be4cbdfebdeb3d2c36cd3f501448db00d2da598014b301af44717`  
		Last Modified: Mon, 22 Sep 2025 23:46:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3ead32627cf4319f34be765ea956063df461adaf2bd5edebbf3b61c239ae5524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a401bc263161648d220d0c49f8f7a382e8ab01f9d31882530b0319b8d5ab27`

```dockerfile
```

-	Layers:
	-	`sha256:41816efa49d3ac30ea3636f10f347dff6925940edbf1ec020a7ebe789ef1c5b0`  
		Last Modified: Tue, 23 Sep 2025 00:35:17 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:295ea450969c40306c28588d824db065c14c7c92a281bcac8133a2cb53abaea9`  
		Last Modified: Tue, 23 Sep 2025 00:35:19 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c35717b0abd9bcd5d2530abf939162b283d5d1531893e1c521ec276702f84782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240435566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80799ac01ad81f7d9e14908dbd71eb09e568c4147d00cb6cb4cf2e8bdb65707d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab906d49eb3640c507c3cc478ea810a9d471bb5c1d173f4a3784926d766ddb27`  
		Last Modified: Tue, 16 Sep 2025 00:43:38 GMT  
		Size: 132.9 MB (132852819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4899eb35084db606a4dea42ee5b0dce11115c460e25729975a279eadad8b7f43`  
		Last Modified: Mon, 22 Sep 2025 22:49:28 GMT  
		Size: 75.5 MB (75513342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c805bee081d5f21fce2a1cc4aac14cf8a58067e385ed50f9ca0998e385262e`  
		Last Modified: Mon, 22 Sep 2025 22:49:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:affc2ea4e23484b358aa50669bbddf161919ba574fc445586a513f20159eb901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787d364691812b6bd9e54b470aa0f3e123f1768d2d5bb0244028baa4a893331b`

```dockerfile
```

-	Layers:
	-	`sha256:8ac210c41ad0135a993454635ddd90233fe6788de8d981d575548d5d6674b875`  
		Last Modified: Tue, 23 Sep 2025 00:35:24 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ba2667d73f25c5ae1978004823380a748ad80e12ead060dbda9f8d2844012f`  
		Last Modified: Tue, 23 Sep 2025 00:35:26 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:89e95621f140a37384b7c4e69ab3001e968e90540dc5ae44fdeb0c5553dfb494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220998119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457a67839d9b16176760a044b251785a9af5acd80aa4742d190958c0470573a7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa91fac631cb7df3dcf58b3506a2d70f536ded0a7815d2e7521e857d5c57d5a2`  
		Last Modified: Tue, 16 Sep 2025 00:17:56 GMT  
		Size: 125.6 MB (125622230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401c35a88bbf815f7cd36e7e30312d4510325396de02d6c22ea6938d6c9faea6`  
		Last Modified: Mon, 22 Sep 2025 23:00:11 GMT  
		Size: 68.5 MB (68490947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a09bdc4778d1760ee6e04fbb1e00709180d96019e25a35996e7e431ced87d8`  
		Last Modified: Mon, 22 Sep 2025 23:00:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2da9bc77ae52b847911713756cc089801ed5d37d6a1b3487e7226dc252e11bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f41fa7786525ff20f238a8429ace317b4a2ba94693b00123851a1d178b411bf`

```dockerfile
```

-	Layers:
	-	`sha256:67b80d362769e140bbf47c1e93fb3a1e422dd8577a87984f79247d9694435ba7`  
		Last Modified: Tue, 23 Sep 2025 00:35:30 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5cb3f75622aba0db0f4070b55ee3e6bd59196e0e9af91fcadc8ec695f0c380e`  
		Last Modified: Tue, 23 Sep 2025 00:35:31 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json
