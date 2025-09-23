## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:d037eed6a39776cc91b8caa0661c687e2a7314b797fa49e2547ddc50e5815a6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:efae49c08133d32a9f1342ddcf7134d1e7ffe6eef74757df688729b0f6040295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156491559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1290ca2dea4cd881790bfed97bfbd6246ff98f9e0c9484eab7ce36b59309ff70`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d0bbf44dff1c427da06c095d5ddb4042987ab49b56ff6d5897ea6b1a38e78`  
		Last Modified: Mon, 22 Sep 2025 23:45:18 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b6650e7beff94fdf4b2f252734bbec12e2364ad4280ba8af70b11367f249c`  
		Last Modified: Mon, 22 Sep 2025 23:45:06 GMT  
		Size: 72.0 MB (71986111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4791a8708e101a11975d588c2fc3e20563454b928435389a97f912fee9892`  
		Last Modified: Mon, 22 Sep 2025 23:44:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0aa78b7015b0725528e2862e0e6cf0d7d8ae8ce212ff4f60a4bf749d499bb26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7422a40c4d29067604a15e8bf4f0dec2901d18d8bdce477a385588aa4169421a`

```dockerfile
```

-	Layers:
	-	`sha256:2207276fff7dd178c7ad87e2d4b46241dd24bbbcf1b7ce6d0649a077c6003a76`  
		Last Modified: Tue, 23 Sep 2025 00:48:02 GMT  
		Size: 5.4 MB (5377723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9016eeca3ac8d31be08181df7144125e2fd2ca1811ac4f8e5dae1632889271e6`  
		Last Modified: Tue, 23 Sep 2025 00:48:03 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:93d2d6bb9366971e3c18f79df42581c564ec6cfce66738751b4f32652e77bc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155777559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e544b521f32ee1f33790b0f66f71da19725cc5e60a10d2a28024728eb54283`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6474fd907852af54a3c8183bd2a24cfc5a6217175821d64425d2d081492599`  
		Last Modified: Mon, 22 Sep 2025 22:17:14 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649d2b83b5b9bc898b6205a328dafb001a4d92d22878ccff8e4e658c3384263c`  
		Last Modified: Mon, 22 Sep 2025 22:17:15 GMT  
		Size: 71.8 MB (71804674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2302db439f21b21105ec2f0a1cfad37385ed2505c01476c738db06ffa66429`  
		Last Modified: Mon, 22 Sep 2025 22:17:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59900bb728261c45f07a1507e06e1c218a7d1d822433ea3835e645fe206e8317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b46c44ae73f185a4a611b59a987d3ad156002175c3e64367e810531f139e065`

```dockerfile
```

-	Layers:
	-	`sha256:d818715d59234a6e704d22fdc6b69f15104b9c11c34b0126417e3d863939cb91`  
		Last Modified: Tue, 23 Sep 2025 00:48:12 GMT  
		Size: 5.4 MB (5384190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e7fdfd01ecc7c8b21ba85875c22220d37013f1e583b471d18d9394a15ed5d4`  
		Last Modified: Tue, 23 Sep 2025 00:48:12 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:15e21d0340bd50e96e3594b367202d0191c13f7c9c88b17e40e1606c59209476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163167336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ebbd58e2b368cc9de8ef9c89810b2b08675c374328c45f45aaa5c0410ff679`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9594a17f6d492bd2de8476aeede85d31ea493e730654abd0387d1bd172577f`  
		Last Modified: Fri, 12 Sep 2025 23:50:56 GMT  
		Size: 52.2 MB (52165369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07770c8cad04c72c4ec9ec827ba05328b381255aaf4114aad654d994927f6c95`  
		Last Modified: Mon, 22 Sep 2025 22:45:23 GMT  
		Size: 77.4 MB (77406970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def39d0a0e94f5368d43571d2ee2a0edd4fb5f68f9a172583d5acbca2a247495`  
		Last Modified: Mon, 22 Sep 2025 22:45:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1235e122a1a88ca523631a547dc950601f92f74822ecc10f4753cf67f0013cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d03e31b10654b4a56fc35dc690d0fe46a3f953e0540c7757bce29f2187e83ba`

```dockerfile
```

-	Layers:
	-	`sha256:d9023d38990e2897136f85e1899fa27e26c7ca5dcb24fe56dee940182dd0dc1e`  
		Last Modified: Tue, 23 Sep 2025 00:48:17 GMT  
		Size: 5.4 MB (5382687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301b0456fd4db62e9c630b67339a48a0ac6afd7e51cff12590e4376fae548a38`  
		Last Modified: Tue, 23 Sep 2025 00:48:18 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
