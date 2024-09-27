## `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:a69b4fde55de756408f6c96e805dd4b73030c6b04ac2dbf7f6e404dcbcc6cf5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dfa8611611a6e24af07682a64dd4ce63a93cbc82e81188798eee3d04716c8989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255091699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0dd8b8e62114e626b3929f1ccd0ab61a53d5c7ce4ea79e76cffecf0e1b7a6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c4b4341317ce78e2386faf285086f80975eb89b15250f1cee5003297f5873e`  
		Last Modified: Fri, 27 Sep 2024 06:01:25 GMT  
		Size: 156.5 MB (156481613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6190a9957f04c91762fa01ccb4394048e6d169cb22b2a9b4215457b0fdf24551`  
		Last Modified: Fri, 27 Sep 2024 06:01:24 GMT  
		Size: 69.5 MB (69482773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05895ca1ef7f9dd707f8b9ad22efb724b53afef8e7640fd67ee1c65df6114262`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a59ab7a1c1a072976852228bad6b283c729d6785704eb0f4380421240f9db`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d51a4eec9ffdb17e562bf58970ae673c9408659514f6f8ded840e6c8f2937bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4914067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4519348cc8ae1f0e278a71b66e2b053c19bdb53aaed40694464520debe0b9403`

```dockerfile
```

-	Layers:
	-	`sha256:4ba26c172e4d2b0035d5a897ad2db3244d9726c0ea1440006437e6ea953daa88`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 4.9 MB (4898554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a9b891b1bc6bb17ad6f730f6c856e246d485751a0e0d8017cd415730487f96`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73fd6ef40156e337a33fae791b5167c0b43d8c50c2baca598bd2c9117cfcd749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253005974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598dd4c6b12c054eca53c683cc8921e9622943b9fa1c083673b9fdb00c92be85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b2ca3ad02bc27e2d696418f91068457394caea057919085f588b3e25db52ec`  
		Last Modified: Tue, 17 Sep 2024 04:52:52 GMT  
		Size: 154.5 MB (154503758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237e40a46a0cfaf7c94b908c7531bdabb5a3d8380a5b356f97e62a91ef0b1595`  
		Last Modified: Tue, 17 Sep 2024 04:58:34 GMT  
		Size: 69.3 MB (69344626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f0a2dd615d0baa971571545532df298facf68ea314b701cb48f381af5b621`  
		Last Modified: Tue, 17 Sep 2024 04:58:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac166d6befc53dc196640a95a01a9e04cc003e63ad3207d6534372e90c81cd`  
		Last Modified: Tue, 17 Sep 2024 04:58:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fb4e4111fd7efc135d4ee852f3d116e173a4fe8691a21632f71d46c334f0124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aabe4cdd6ee00fbd7d332edbba166c04860cd2148f6af816a1118ed537dc9d9`

```dockerfile
```

-	Layers:
	-	`sha256:91265c1eca341cf90dd3d8512c1ac7c6c9f8efbb229afa32ab73e2a9ab02157c`  
		Last Modified: Tue, 17 Sep 2024 04:58:32 GMT  
		Size: 4.8 MB (4751571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61a9b44aedcf6617872f6dbcd1f63d6750c8f678b41009ddd8acbdcbbad2a773`  
		Last Modified: Tue, 17 Sep 2024 04:58:32 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
