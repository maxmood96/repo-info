## `clojure:temurin-22-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c538871cb90954ab88e597285c345cfe7800ac3c960fa82ad4bd93c9cbce3df4
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
$ docker pull clojure@sha256:7546294624624baa4fa2da7ffbf748e6ad04d6728e7fdc12e9ffd1b21510f120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284301662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48bea0f583123f10facac86f9fa7a328e9a5a151c844e33372be5075deb9d1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ae9ea1ede1da6ae0a33e9e1cf1235bfa0a08e3a3467bd0accf3d434e39dc34`  
		Last Modified: Thu, 05 Sep 2024 08:15:42 GMT  
		Size: 154.5 MB (154503755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89cc45d388d4bb630b84409427349c25582121ad95cb2f46a403546b445796`  
		Last Modified: Thu, 05 Sep 2024 08:19:32 GMT  
		Size: 80.2 MB (80211241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928805f04de24d3964aa0bb9be1a47dd9ace2e4781cf85854aac9f9ac8e86d73`  
		Last Modified: Thu, 05 Sep 2024 08:19:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772b3476f60e10b1a9a881b1f32887c79189e9a0e0f968dc8d2c8bcdffa29b92`  
		Last Modified: Thu, 05 Sep 2024 08:19:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:809349787d548de2406892b0fd3ab264a47eb0f3e8350fa4f92a43514c21bd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446d3e7ec5d0457a2190ed07f50635756857d46588014d7d5efa785d2a8e9866`

```dockerfile
```

-	Layers:
	-	`sha256:cc3a70e6e1872b59d49effc5c3f05baa9ad135dbc7581e89bc01f6e04edeb03f`  
		Last Modified: Thu, 05 Sep 2024 08:19:31 GMT  
		Size: 7.0 MB (7006560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86592c789808aea2d301f5845c8a257d2b8d935c021cb46c6b0d2e9bea85f8f`  
		Last Modified: Thu, 05 Sep 2024 08:19:30 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
