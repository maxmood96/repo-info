## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:0590d085d52f1e9ed228f2b91fccb1c80be2c54ed0ee312085d137faef6a26c2
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
$ docker pull clojure@sha256:37e2ac9fcc60ce956fa04561bfccf297f62e1d4765d5bc3618e27722aa7d7535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240590859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7e621fdbd32e0347c2752fafa7190209ac79244d7ee274f6230b59cba63fee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b09e1a9dd798a45459f926ad8d2252d7874c16b30997fd9b3909132732a599`  
		Last Modified: Wed, 25 Dec 2024 07:25:32 GMT  
		Size: 143.4 MB (143360951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa51f3fc1e3c396528855d0c45f3f14128d697fb80552eed9d6bcdf059f80545`  
		Last Modified: Tue, 07 Jan 2025 03:27:45 GMT  
		Size: 69.2 MB (69170146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c209260cba2b81d679130785391d6b78aac96568a2032bf14e96754279e5c8f`  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d54a7d877f882e31c5a97409e7bb3e57be0f39c93adc61f54cb756228cc0f4`  
		Last Modified: Tue, 07 Jan 2025 03:27:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7392dcb8281c53aabbcbbba412164c99776f857c320f199eb631a904e522b191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7afaca4f9526b7a61bc84a4cfe7b38634e2c61164fdbaf8214b3c49c98a7f9`

```dockerfile
```

-	Layers:
	-	`sha256:1fad92dddcbfbf896b728310526df19aacb8f55c47486157401eba287d1ee50d`  
		Last Modified: Tue, 07 Jan 2025 03:27:42 GMT  
		Size: 4.9 MB (4918330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1e474f4c36005a7c33158568a2a2ba9ab829b1dd1bcd1890a1bc3f878b31ef`  
		Last Modified: Tue, 07 Jan 2025 03:27:42 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
