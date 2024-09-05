## `clojure:temurin-22-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:1e47d27ca88f7fb5810be0643813473bf9ddb9fdc258f8abe4479f041babc564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:33717b76aea4c5e426aebe944d1f2f64ee1b4ca24c2c5e9a089dfc27112fa115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286505440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff432028b3d7414e8fb7f18d4f47664180b05be16469bc9da5ff29d95bf6c54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4ddde6d79c6bbbb71f7ea373217602c9115ddad1b476e9b9142f29ab860122`  
		Last Modified: Wed, 04 Sep 2024 23:08:17 GMT  
		Size: 156.5 MB (156481615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e268096d991cf36a8d668cf2dbd02ec23d4ce5285a372f95df8d7f6d281f0d7`  
		Last Modified: Wed, 04 Sep 2024 23:08:16 GMT  
		Size: 80.5 MB (80466082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e69c6856124c783bc1aad109df76d6472e85bff60c6176b864a2729e02eff`  
		Last Modified: Wed, 04 Sep 2024 23:08:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5ba5308995da35a898c0d46e40b96148585b7b0c498f98f4fff7a7ee0db873`  
		Last Modified: Wed, 04 Sep 2024 23:08:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:26483c388d1de4de1c2d04bd4b5b72acca4ee3fc4ab16bea049ed1e013d0a050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814a157e2a358941b8d798a9be5b61a9be4a1202a00b0f8de666fc2b6272cc3c`

```dockerfile
```

-	Layers:
	-	`sha256:fd703a3aa2b8d2c0a99bff59fffdd06fe4230ee2ff93b9a4d29f4cd9e41c9d01`  
		Last Modified: Wed, 04 Sep 2024 23:08:14 GMT  
		Size: 7.0 MB (7000149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75928abc70cbe29ddbce877b7bd4a0bba1883a0b8affb35b7d3b677a1f57ebc2`  
		Last Modified: Wed, 04 Sep 2024 23:08:13 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:994959c45f27bb4824338bdbc43e812a9047d1939391f25f59f0e68163bc8331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284291771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f211537bdbd3cb41a325d11d07357a9361f96014c35dc9ea4d8d47e612bceca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648268b85fd4c094d06e828855a5f546b3a97f5c94583775fd9a0fed4c242a27`  
		Last Modified: Sat, 17 Aug 2024 06:33:14 GMT  
		Size: 154.5 MB (154503694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50846f3a5fca54082821717a4db25aa4a3390e5831aef8009a89fe11be735dc`  
		Last Modified: Sat, 17 Aug 2024 06:39:02 GMT  
		Size: 80.2 MB (80198444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a6f74b6c779ba710163511bd97a34f5af70a635e46421e6d51d67d469876e8`  
		Last Modified: Sat, 17 Aug 2024 06:39:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4930b8bc09e9c4bd63a75bc59a444277bc5273fd9e881c392240a8c703e2c79b`  
		Last Modified: Sat, 17 Aug 2024 06:39:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f5cc6268a672f1676044e536dc63d2846624aa4fa688d74e779209ce5d5dfaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b878264c91a0e5cba629bcb9ee5ab0355fa2942817b734fff74c9deb228a2f`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bca5bad6e629e8a90fe5c19ea2ce549a683be0774c8a84177eb2ecbf4ba8`  
		Last Modified: Sat, 24 Aug 2024 00:10:37 GMT  
		Size: 7.0 MB (7007175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cca08ec5987fdb3340e9a6cb79d0977ae16e18e26d69a9409479b1dbf39420`  
		Last Modified: Sat, 24 Aug 2024 00:10:37 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
