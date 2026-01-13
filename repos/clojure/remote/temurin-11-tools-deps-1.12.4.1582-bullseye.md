## `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:6a45e57e424a277c32342c157e7df0506685083b0f42454ca63b0adaa7f99499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d0bd0fe6d1b66a882d015afde93f7b1d75fbb581dcec8572c80a5efadbb5a380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268280457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd17dfe812d53c61a82acdeefd96fca06f7bacb519c9727d106f1b4a2865320f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:24:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:24:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:24:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:24:18 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:24:18 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:27:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:27:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:27:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ff4cb8f2a70ec11be8124e6eb0f2eeb14f2e6e22fa2b50f625b2c2f4a9fd99`  
		Last Modified: Tue, 13 Jan 2026 03:24:59 GMT  
		Size: 145.0 MB (144966609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49c05a976a5e34af262628243d90f7037c12d92357f4620abb0a5be2eba83b`  
		Last Modified: Tue, 13 Jan 2026 03:28:04 GMT  
		Size: 69.6 MB (69556757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c18492a4965caf2c4abca025ec5a16762415dae71eb87901e46d7b05c17515`  
		Last Modified: Tue, 13 Jan 2026 03:27:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:096e9d768ef799ac176b1c9f7f07e6c1f49ba29e94b90ea4625d74066c6a9d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e853283332da1a940c4847bd30a5cb0daed3eed392d7f9912f79fc309c1c12a8`

```dockerfile
```

-	Layers:
	-	`sha256:4cde7b965621ec41de74f5fc5117a6eae8d8734dd1699564a3dcba86f6fedf03`  
		Last Modified: Tue, 13 Jan 2026 07:36:49 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a777083c58c6253b0bb06026ef2adcc21a12bcba2b4ad7a305a127404ebb30c`  
		Last Modified: Tue, 13 Jan 2026 07:36:50 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e73a084e8fda14ebbed357c6ed7120be9adcc0b330aed59b6f427efc6037725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263676917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a282eb7f8a071a0872f755af7b8c39a744a81b220831017eb4c4019b1ba8720`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:31:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:31:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:31:45 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:31:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:31:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:31:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab165d25dc394c7e7fafcbfa9e6c1d132479f5e4be58f1090e6be844c36a9b83`  
		Last Modified: Tue, 13 Jan 2026 05:31:47 GMT  
		Size: 141.7 MB (141731578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9219bb9ae73261abef49feaae37091fbf740fa876e58c56f4d0ddc8bd513f579`  
		Last Modified: Tue, 13 Jan 2026 03:32:34 GMT  
		Size: 69.7 MB (69686924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3932678c25b176a81e63e5b0d9ce45031690ca507485b337a9a5fdd3d9a1ea7b`  
		Last Modified: Tue, 13 Jan 2026 03:32:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:68e95d0c0044dbbf511370136a379f2dbbf4bb0f00b6ae1bfd7e857038eaf2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1ee320c72ea76ceeb691dd3012b6020f7704b71f534b4884ef38c8b0632c58`

```dockerfile
```

-	Layers:
	-	`sha256:6f8aed0ec1082e05d99586b5e9d8ca85b97676fa00d6e20b2d4ad47537e02ec2`  
		Last Modified: Tue, 13 Jan 2026 07:36:56 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9b70d48722054e5182043de84548988fb4807a469390db954c31f8540ea558`  
		Last Modified: Tue, 13 Jan 2026 07:36:57 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
