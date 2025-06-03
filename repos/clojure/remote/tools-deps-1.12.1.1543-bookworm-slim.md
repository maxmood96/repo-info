## `clojure:tools-deps-1.12.1.1543-bookworm-slim`

```console
$ docker pull clojure@sha256:77c8d6eb40056d7fc37fac3ab8d70de398e89f63dd5049c2f27df304a7b256b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:tools-deps-1.12.1.1543-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2340e3a396678fd47268b1abdb844968b6db85342c7e7153ac9c5653ee70be99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255390313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56feb9c1b307e5c58f5219a0fcd99ef7c1271784eb489e9df6ff12af8f49b33e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e7a4d4234a0b4690c5915a6d5517f2dd6652988554214cc8e8e255691e7cf7`  
		Last Modified: Tue, 03 Jun 2025 18:24:21 GMT  
		Size: 157.6 MB (157634483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76361398bd7a36a4113496f96e680babcaaadaf0128aaeda0723a2831046f917`  
		Last Modified: Tue, 03 Jun 2025 18:25:11 GMT  
		Size: 69.5 MB (69529459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc57f53ae751fd395dfe8c11bbf869d6f8c9c871aec5b28e847814e06b74db2`  
		Last Modified: Tue, 03 Jun 2025 18:24:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38261d2c941233d29f343e69dcfdeea536e3e0042bd6c21a0a2026f2ab062ce7`  
		Last Modified: Tue, 03 Jun 2025 18:24:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1543-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60fff831b390d512f8fc89e556d07fd2843b1781abb70d9b3ba180015e7343f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4981869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cd3d09f4bb1ee80217e6c7ff5b7c158944ea11f826205ebe91dc2a14a2f7d0`

```dockerfile
```

-	Layers:
	-	`sha256:93afaff100dcbd00e10cdc50b80d2e054c435eb744dcd3ca2d467f733bb8b142`  
		Last Modified: Tue, 03 Jun 2025 18:38:37 GMT  
		Size: 5.0 MB (4965296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78dade58da4966836659473d63a5d51dddee854409917efec1ca2fd77a3d12ef`  
		Last Modified: Tue, 03 Jun 2025 18:38:38 GMT  
		Size: 16.6 KB (16573 bytes)  
		MIME: application/vnd.in-toto+json
