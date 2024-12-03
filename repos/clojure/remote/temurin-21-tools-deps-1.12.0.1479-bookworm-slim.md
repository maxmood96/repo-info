## `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:15ca1c5c74b3c2236cee735f71d39fa0f0321588d5812c2e18391fbce74c2f20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3ec313454b68e581027c189233ffaccc9a3cccc9e015c99f7a289bdf6024c895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255094149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5ac8a4962c32b357a6c31459c8fceba2871c0fb6632499d0bbaea8b63953cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feece9d44b953a4fa9e90938981ecea78008c56668cfae7cdb4af337d7660447`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 157.6 MB (157568689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f062ddf5e4652a3c6cf6bf263d0bec22a95e8fa6cf91907bfc59473815070e1`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 69.3 MB (69292839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69caf328c24bd21b8b41300dcafd120ab61f2619ec81d5474b550e1dac62c81`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314e3de50d576bdc152d74314aa22244ce9a5d9e170d1fbc69c6e9f2445810b`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a34e2d65df2a92ecfb0d63ff655d2dcb2d6e3fe7ecf4b1dc74650ef58b0d4446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4939756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde828e11aac37eb3bef90bde2eeff02b35440e2bc4bce901fccf7f99b399869`

```dockerfile
```

-	Layers:
	-	`sha256:91622e8806e4a833759d3c5427b7b13052f140f62718ab608c39a948dc09ce8c`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 4.9 MB (4923183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbb0b4f3a76a8a26ac9639bf2115af05f44534b294528e634088c99e21b67ab`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 16.6 KB (16573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46dbfe38b01d8b4368a58aa947cc7e299c3eca9c90ff1df4750de34ec5d83f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421c97b051f2797873dc31a4ac6b596beb7b3508f2548aa355f898177eec39d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11788338479823b777f7adacb2addcb65dc2a80dd644d7561877d39b5224b474`  
		Last Modified: Tue, 03 Dec 2024 15:25:04 GMT  
		Size: 155.8 MB (155793088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f414b3a529b9085d04ac429d6439e410acce19192fa235ade010718889018b05`  
		Last Modified: Tue, 03 Dec 2024 15:29:06 GMT  
		Size: 69.1 MB (69140792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d62f54cf2de67d5b750ca8d8b9eed267934bf05d6f5609ca566787a77564d3f`  
		Last Modified: Tue, 03 Dec 2024 15:29:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3515e5344a3d0c414d1e0d93d8eb57f57e65f1f1bb7dc87a8e472a9bc8591d`  
		Last Modified: Tue, 03 Dec 2024 15:29:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32cadbb516c528ab97c4de2c27a86dcc99a2233d0bde0ccbe4d72cc129a55632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5f73ef16e761a33ebe332c5fc9dc83a4ffedc8176215f2cfad5df92ddc57dc`

```dockerfile
```

-	Layers:
	-	`sha256:4825148d07285287b69ab0fc87d858c4b41df8250fe03fc249d6853cb412fcd7`  
		Last Modified: Tue, 03 Dec 2024 15:29:04 GMT  
		Size: 4.9 MB (4928973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bdb17d6af6b5e30b91068150a4705694351ad395f51b5553f08ca2fbb074640`  
		Last Modified: Tue, 03 Dec 2024 15:29:04 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
