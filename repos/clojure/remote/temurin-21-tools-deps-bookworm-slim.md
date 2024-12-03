## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2ff10b8a77ae6c1ce255ecc2b06081fb2cf43394dd7b834f2c97d79df77ab2cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee7ef07d6c2ab36fd9f3c2bf31a6b03fa14e7ab421b6e7cf4dea40059755c28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254286240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6916ab1d65fc87ae289b2a38350d9749faa9a008d8f56f617d170f81ddc96363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f7539dee24a48611ac02187ae2256212e947bf77784c765e04b2e40e3962bf`  
		Last Modified: Sat, 16 Nov 2024 05:38:25 GMT  
		Size: 155.8 MB (155793074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8211ebfccbf5d7099e43767466885fd641a6ec3476c6569e5d2c9a1fc142c2`  
		Last Modified: Sat, 16 Nov 2024 05:43:06 GMT  
		Size: 69.3 MB (69334769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239bf7c2b78b8bdad07f1ccf3e22a122452cbe25452605c5aa120117c0c627b9`  
		Last Modified: Sat, 16 Nov 2024 05:43:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e39f70758610f0057aabe665649561acdee392357b1ec9f7159c826e19fcd5`  
		Last Modified: Sat, 16 Nov 2024 05:43:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d845007f43574942541bec38094a5379418fe83375fd70f77b687694cd3de5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77058c63467c623b37eb124fdafb372142a142041f0f6b4a6a8d3533a0616c0c`

```dockerfile
```

-	Layers:
	-	`sha256:13bc6ccda15d73c037910d94a55e1a20024c8a828bbe47ee21b5b414c3bad01f`  
		Last Modified: Sat, 16 Nov 2024 05:43:05 GMT  
		Size: 4.9 MB (4930221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee748580c99c627f3111a727e5ee2168a2dd48353acd7dd2dda47d428886e6c`  
		Last Modified: Sat, 16 Nov 2024 05:43:04 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
