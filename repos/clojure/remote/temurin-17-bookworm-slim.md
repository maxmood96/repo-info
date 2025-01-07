## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:80943cf1aae4800a63f9278b62279e199507bf70ec0c6c0bd77e019be3d9f5f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3af55b96e691f3c7dcbad8d88902f8394765d833b08d9262b06780b2b8458e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242081447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa1fcea639be6becb4d5d56793f28e8417f22985a03aaeda1d5a0acac4ad125`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca30158abbec3b5ece744d5bd2a0cac015012b7d5c807f2e9bbb6427a482d05`  
		Last Modified: Tue, 07 Jan 2025 02:29:29 GMT  
		Size: 144.5 MB (144536666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac634878311b9c98406ce42b47752ba54f914bda59e25355c32a095c912533d`  
		Last Modified: Tue, 07 Jan 2025 02:29:28 GMT  
		Size: 69.3 MB (69312160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ba52f3202736bb11965d59e56144ec2ca5b690a6a455139de5a635413ace5`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372c1204b297bf759703fc9ac063764f5e0974d6cb00da94322d541800b0eb5b`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:071799d01e347b93ef2aad3f6a7b6fc67e396dee1fa11f2e58bf386d35d2f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7933bfb8c41909603b3e20af0d3e0794405c465ca2a8a034c707ab65ebea25`

```dockerfile
```

-	Layers:
	-	`sha256:664b94bcefed45f1155f14a07fc1056ea0fd8af563641c639d117b15a641e9b5`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 4.9 MB (4912569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10949cfac9316f3f2a4cd809fef65e1755833d8a7dc3b6b0a948c8a570f592e8`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebf866f2cc78d3701a6e8fa09ba67ceef69c7821b3686f08d16014a3388835d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240561629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b762cb6f4a4d3f2977a6c057defad8034a08396838564f1584be59eab05b0e02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b09e1a9dd798a45459f926ad8d2252d7874c16b30997fd9b3909132732a599`  
		Size: 143.4 MB (143360951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebe446ae1f5aaf8c66d1673be5e8f5bac929bdbc77c7dc8ba7e6c9d001e9ce7`  
		Last Modified: Wed, 25 Dec 2024 07:28:42 GMT  
		Size: 69.1 MB (69140918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e234d75d03d8cac5f2241b2de29222835556976626b1c25d41f907761eddbf2`  
		Last Modified: Wed, 25 Dec 2024 07:28:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d19f526f2db85f5bb77719522ff6b97930f99a0a8fc3fb0b3e8924736a1b3e2`  
		Last Modified: Wed, 25 Dec 2024 07:28:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a459632a40e903f4307a962fcf75f12c74e7461b151a5213910cb5e56fb6b558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33aba1c7c542da424c831ccc4969c5d4f7397547b67fba55ad79615383a20b6`

```dockerfile
```

-	Layers:
	-	`sha256:aca427cc4aa56b00f16ca735356acd8382fbebc5e571202afd1261307c7ce0c7`  
		Size: 4.9 MB (4918268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46751357260820b6117dac2fcf399c23707a8be9c077ce6be7bbc614ac0e3573`  
		Last Modified: Wed, 25 Dec 2024 07:28:39 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
