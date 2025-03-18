## `clojure:temurin-23-bookworm-slim`

```console
$ docker pull clojure@sha256:fb15910a0117c8026d39ee0904592731f22ca6e0e56754943c2ea9d8dc110f7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ef8c6ae457af619972f69b5729230ec330eecd68045bb68110395c784da05e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263050446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985a676908ebbb34a5cbee7818aae3d5bc7e2d29d2d642a0ecc960c8fa310346`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3c02007a17115b0ee56b92f654e41eccda6fc9633e9fb70c632d49488b357d`  
		Last Modified: Mon, 17 Mar 2025 23:21:53 GMT  
		Size: 165.3 MB (165316166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f392df3c5c44f60605c45ec052e856e0830a0ed2366fe3d1cdb0018c2290f3`  
		Last Modified: Mon, 17 Mar 2025 23:21:52 GMT  
		Size: 69.5 MB (69528374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c73b0fcc2add20846711530686eab932a5bb25dfaf46811c73f0b5528e89a4b`  
		Last Modified: Mon, 17 Mar 2025 23:21:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a63e3669d321d8dc0e05bcbd88f477aeb8f53fa222795614cc42181ebf13866`  
		Last Modified: Mon, 17 Mar 2025 23:21:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6c9b21d763853da01e3131b830f3e52525e59181ddb9a54b71e2587584f3a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5928901633721dd7fb3fa9360ff51b503a9a41dd8d03a6491f30e79ee31b9a2`

```dockerfile
```

-	Layers:
	-	`sha256:02d05b261131f073a7ed776c3a6ae50f63cb8746c0c72c40126b5ba1bee2a107`  
		Last Modified: Mon, 17 Mar 2025 23:21:51 GMT  
		Size: 4.9 MB (4917602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:267a59ad21a3a25ae7a828b80b038992317df084e0678ec773798f099fb1b2c4`  
		Last Modified: Mon, 17 Mar 2025 23:21:50 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c1f9f4b57f8429c5b6e6182c6a40997163e958aba8b9f97c251beb1e98a7612c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260764169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce4f348f18a23d5ad14f92cc48c66610650d867591304713e6fbd563712ace7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03199da6969e31e419eb82b3ea161a6437ad00bd56fb6aef934c5ba9c3492d`  
		Last Modified: Mon, 17 Mar 2025 23:43:29 GMT  
		Size: 163.3 MB (163341467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9478f109689454a7ea8cbd361d5b27a8175913f1b114b1fb7a1c42bd4d007c`  
		Last Modified: Tue, 18 Mar 2025 00:01:17 GMT  
		Size: 69.4 MB (69377623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f41d5a64dce7e03110a569e55f44724335bf4269a0784f645ee03b05723437`  
		Last Modified: Tue, 18 Mar 2025 00:01:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222fa24d864130f26091d7429e5f0b11ba3429acb4c0dd71abed7fa2aba100b5`  
		Last Modified: Tue, 18 Mar 2025 00:01:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e74970c7bc11473124e0922c702f53e8aba7a10a54cd3b33380135f8d8689767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66cf8348eaae1ecc96d91b4918cb1978da939cdb141bcd89c88bc354731b226`

```dockerfile
```

-	Layers:
	-	`sha256:64dfe4b6bee46922b7e3208a6e1ace8f1e59f11dd76f6daff15c0f979910d57c`  
		Last Modified: Tue, 18 Mar 2025 00:01:15 GMT  
		Size: 4.9 MB (4922742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64fb01a5a8f80329cbad6f8cbcc0f43f8ebc3f370446f9c61dd156bafd73f789`  
		Last Modified: Tue, 18 Mar 2025 00:01:15 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
