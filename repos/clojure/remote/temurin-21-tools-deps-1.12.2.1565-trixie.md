## `clojure:temurin-21-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:619c5c57ae437cae5c9bbf292f7cd10270bc196caf8f0a45efdaeecc26187a01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a2d6cd895b20b867798cfb9a479e282272bb6a4e589235ff70f04222a6eceb20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292617024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de8b14d80e92e88e0c10fdc1bd581baea6c0738b02ae09306a4074b9dd72863`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a769a98e579a2100eaa475cd72cd62380ad80aefb4ef0eb52da66fa379990d67`  
		Last Modified: Tue, 26 Aug 2025 18:46:10 GMT  
		Size: 157.8 MB (157804749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e53b83141cfaf9cbd73da8a54875f09d4da382bb3a23428288a6f5d709ef88`  
		Last Modified: Tue, 26 Aug 2025 18:46:10 GMT  
		Size: 85.5 MB (85532954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44090328e874e3cdf78f008323914c9cc56b42efdd751f6ed6c1c9b9eaf350f5`  
		Last Modified: Tue, 26 Aug 2025 17:32:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d9c6cd2d32e2489bfe59cfc4b605c1c1934c17f12d8c666ddcad80cc817438`  
		Last Modified: Tue, 26 Aug 2025 17:32:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1dce2db39402826c16e03dbecf66db43f4a80b7ddffb99b70f89ec9372ff0d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16eedb8bc7bce895ad54ee774a38d72101350958f1ec8b703002ef5f17f0342`

```dockerfile
```

-	Layers:
	-	`sha256:a65e76963543a403558d49d0ffda374c877af1daa67e586d2e29203764c7b118`  
		Last Modified: Tue, 26 Aug 2025 18:41:06 GMT  
		Size: 7.5 MB (7465991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8911e46c48a368269018287c5afa024598e09b7f6ea2c77feb24ee0f4902aa74`  
		Last Modified: Tue, 26 Aug 2025 18:41:07 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:72bd780acf07223f99297122e2ea4f324341aa8316821265916004b2958b9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291080530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a90e7609ff27dba55ae7ed783debc0dcd73201d5997767fe6d6714d97b9aae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dffd1770ccc7064c174de1d859e06dacb9263f4c3b5b48d7ee5c92344915b6`  
		Last Modified: Tue, 19 Aug 2025 02:31:02 GMT  
		Size: 156.1 MB (156081252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e4d871693a3d8bf4f7aaf1a491e525aea6fb43b438cc9545a3504ceee31e89`  
		Last Modified: Tue, 26 Aug 2025 17:52:33 GMT  
		Size: 85.4 MB (85356632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8455b7a243fd0b5e06fad2490c27be0f0f6c0ce8c77db506e3030f23768bfb`  
		Last Modified: Tue, 26 Aug 2025 17:52:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae40067dde48bf5747489761e4aadeaf7000b600867529ac957bff2712aa455`  
		Last Modified: Tue, 26 Aug 2025 17:52:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d2edb22b6473f14d3a852318cc6bf55f673a57aad7fbcb1d91af6e67e9aab38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00760ba3ef1dbfae23a44e1d1d7892ae6ad4407e775e6efd88dfb6e802319ac5`

```dockerfile
```

-	Layers:
	-	`sha256:0c8075020e8780bc2f11b1d6a633c97a74bd616ec30170c879b4c5835ad0b2ca`  
		Last Modified: Tue, 26 Aug 2025 18:41:14 GMT  
		Size: 7.5 MB (7473045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0e3b9fe3fe54b8e20096afdf8bedf8edd363d4ed68923bf125ca4f1d68264f`  
		Last Modified: Tue, 26 Aug 2025 18:41:14 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json
