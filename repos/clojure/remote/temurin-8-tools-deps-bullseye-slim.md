## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:58ff4b99fb18ad59200c0aa4b16da910b24dac77dc2ee6f72350c740c385f064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:04e322340471e3283b0555185969651f7403c59372166036e87658938912c9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144611846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775bcbb822b1360f337777b7da198b9881ae5deb7a9ed1e36d9cbbfa50ab708d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:55:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:55:34 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:56:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:56:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:56:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18274e6c2645fd55899846bb8b158083e568f972fabff2cd5754aaf923daddb7`  
		Last Modified: Tue, 17 Mar 2026 02:56:04 GMT  
		Size: 55.2 MB (55170146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e906e19fbb74908cdb2d11c2f4b2892be86d1de0dfe6e8fd4a3cc1a46ba5a042`  
		Last Modified: Tue, 17 Mar 2026 02:56:39 GMT  
		Size: 59.2 MB (59183231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9720689d626e2b16e68c6e98ad688d99c9da99c08a68da096ae40afa555dd7`  
		Last Modified: Tue, 17 Mar 2026 02:56:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6380ac3269d4db7b52b10108631972a3a970964140da9ad16055c6fab7fdf934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af69c10c771812dfe3921140b3cbac58f44277361ecb32a8d6c2304a6e96c80`

```dockerfile
```

-	Layers:
	-	`sha256:74b9294742a63897cf796c673e11280d46d744fd6e8852f20eefc0ccc6a68bb9`  
		Last Modified: Tue, 17 Mar 2026 02:56:38 GMT  
		Size: 5.4 MB (5441040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f397436bac8c3c23e5ec06dcc6bc0606fdf5ee2edaa769ce73a3a012f6758ab`  
		Last Modified: Tue, 17 Mar 2026 02:56:38 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a944d1cd5f33b262d6af9f415f66856dc2f60ced6c25938281566a29f64e54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142320544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54acc1ea44bff0a566f8adf9e3f696594562949256b49dc7916068837cc78a5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:00:28 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:00:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:00:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2510a29728b9b62bae64d8da60412fedb071938803ea40ccac6ccc2a2d2cc2a`  
		Last Modified: Tue, 17 Mar 2026 03:01:07 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2906de2cf456a485bf7091276ef2a083b8e74a9c71f5cd5475e60c74ceedf4`  
		Last Modified: Tue, 17 Mar 2026 03:01:07 GMT  
		Size: 59.3 MB (59323764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adadb299bd404c5cbe649845ff3b9b512d55e590b62ea10039390a1ac285bf84`  
		Last Modified: Tue, 17 Mar 2026 03:01:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f69fd1dce974825da222af47303cdc30762d0dbc9de3981d89aebe6e27bd4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f472e3083a30718cc40e4afb029f55d988fa0b03cbd926ed568959e0b6fb4e69`

```dockerfile
```

-	Layers:
	-	`sha256:e24bc3cd54997268df31aa5193d66d354d993e822cd569084f7e0c40a626c83e`  
		Last Modified: Tue, 17 Mar 2026 03:01:05 GMT  
		Size: 5.4 MB (5447472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effb5bfba6f9338ce3ca34dbc14189a8d148f4f207526cef3d6f6056e67157eb`  
		Last Modified: Tue, 17 Mar 2026 03:01:04 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
