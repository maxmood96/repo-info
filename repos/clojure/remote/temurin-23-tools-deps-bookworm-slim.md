## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2e0f1f2e0af2ac88ae3ae0304878677173d22de3bf8be6986f4a6f61e777ebe0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5f231be50764280969944727c2056118943b56e66514cbee3b25ac0405b19758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263063999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044666ad3b126f9faaa4cf3e9fccdc2e19082fabb31989bfa6856a0462b581a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069596e310dfe895da22fe6575b69b2ccfd2b388d3ae220fd6fd90de51854dec`  
		Last Modified: Mon, 10 Mar 2025 17:40:23 GMT  
		Size: 165.3 MB (165316201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d0ecd8b2ac212c1c3e0d65e5752cfb99a77d2f3cc59545928bfd011e3f64e`  
		Last Modified: Mon, 10 Mar 2025 17:40:21 GMT  
		Size: 69.5 MB (69527455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d2f242046fa1ed63dbd24ea80654f6b1654f3883cc38b53d1404cf8824f4`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c1839af282a0c7d0ddb1763ef53e09b25b8fd46eb8c8c8b15601494c4a5b77`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0656cc9d9041f15bc92f2d5652ac1b1106529b5a40a849c13da0b6c8298bac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852dfb38e9cc026bb49488048a03ecbea24209c47d6284af057ca8fc89077873`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ee02bd1872e487f125957891b1bbde4328f4243922782fcf0f4277bb24967`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 4.9 MB (4917590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f231aec426cd57a83fe0262de4a55dc4b0b0dd1367208d2cc4e0a3a19c1eb247`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

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
