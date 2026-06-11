## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:47b1098b7c3eb3145e19018bf6ed59fc1c6f69e0379a02661993893e13936334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6934298b7e847a4e8fc9b4ac44de54a31cca3f51c6d2433cd45db1c48a85c140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266190529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb012bc16c750fe3dbc92c42830603e1937fc25a9e20e1163f5d4fa1d2908e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:18:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:18:47 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:18:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:18:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea649aef638968056cc3c5a5be28089446984aed01da56d583d22e99a95fbaa5`  
		Last Modified: Thu, 11 Jun 2026 01:19:22 GMT  
		Size: 145.9 MB (145905444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600d26229d61eaf15a4c486556e07a60765cca08dbf767ee9b6ba6633a6f3f24`  
		Last Modified: Thu, 11 Jun 2026 01:19:20 GMT  
		Size: 66.5 MB (66512275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c8eff6d52bf2043fed03ae778f502fc93b64518b8d845ad23507cff5525152`  
		Last Modified: Thu, 11 Jun 2026 01:19:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cebf4456dbe8139889c59a32dc86c519ef364a7fc8a1a2ec0174b5a3a7e71fe`  
		Last Modified: Thu, 11 Jun 2026 01:19:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e2ca3e9fb71d168a5cc5e2f1ee8b11de0357cc976bbe151ad24c84da9202a3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a6700736c7c3fa7f3d96e0153bcbfd0d8029d60aaf551a6ced63a4c9ae09a2`

```dockerfile
```

-	Layers:
	-	`sha256:121abab09d631358c518d47c226d9f4849d3dcfb36d5b164770db6e92b5a9a4e`  
		Last Modified: Thu, 11 Jun 2026 01:19:18 GMT  
		Size: 7.4 MB (7405449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5215cd33bb199f2ad34983b04cd16236182e2451430f71c3eb122a20f32ae2ef`  
		Last Modified: Thu, 11 Jun 2026 01:19:17 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a504e17dcc708d4b1f5409bdd09660355c41a2de7ad53ce1ed20be17d8a7fa7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263667192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455125ce9692a49c49cc09634faf33464cbccde2dd4549909b8c1e561f742165`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:23:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:23:02 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:23:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:23:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518f28ce298c2f7024f9dc9b8cb6f1649ac62955ab5349c969d414e2b07e6cc6`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b17c800d162968f76d2af7d1ea926860f81bf27a43425f332c95277d8b9555c`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 66.7 MB (66677698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe06ebf6beb0721c3b15b2d079f54d886056e8a185ed19ea01722df702342e3`  
		Last Modified: Thu, 11 Jun 2026 01:23:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcd471460827f2844c1b06c54a7cfe9d72a15c006d2dce9d68c18f0b23c5772`  
		Last Modified: Thu, 11 Jun 2026 01:23:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9472917921859c477f49ce736d3a577a76e7853cee2aa3730c566a9042ab125f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4382b890ff1823767decd6d771960bfa181f054c9bf642819ee2cf8dd814bead`

```dockerfile
```

-	Layers:
	-	`sha256:21f49eb9da07d660c5bc91840c56d1d34ec57bf243e2afcd1fa2e2e4f4fde28b`  
		Last Modified: Thu, 11 Jun 2026 01:23:34 GMT  
		Size: 7.4 MB (7410548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e1f2734a284d290965f00599e0edca716a318fd4e49e83b0fe7ea4df40f8a8`  
		Last Modified: Thu, 11 Jun 2026 01:23:33 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
