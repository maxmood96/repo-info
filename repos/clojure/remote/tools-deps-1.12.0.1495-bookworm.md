## `clojure:tools-deps-1.12.0.1495-bookworm`

```console
$ docker pull clojure@sha256:2da4a41790949865bbecce92f3a08d790f5870997c0093f88169476ff7436138
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1495-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b77841aaad98c5e2d4e34e276ae7eade51ef72fb283690dd7cae59f897271d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287027722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ee71dc04d99f94908da35b48c7431f0d7f576d8c30f05126a2f8d2cdd6e43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b2cef08417c048c7620857edac142683a8fb9bfec5dbf9f2350009bc397d1b`  
		Last Modified: Tue, 14 Jan 2025 02:45:00 GMT  
		Size: 157.6 MB (157568674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ead3cb6c01808942915b91926e4296aead4bcfa9c4837d68cd47c8d48d95595`  
		Last Modified: Tue, 14 Jan 2025 02:44:58 GMT  
		Size: 81.0 MB (80978046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d5089e784d01a2225e1a328af1911563657c1331ad8e7a6f8be0f1633083a3`  
		Last Modified: Tue, 14 Jan 2025 02:44:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875d57d8615c22fa4aa654453cd2397e8fcb05d7b62e90ea7f3bbdcb027fcaec`  
		Last Modified: Tue, 14 Jan 2025 02:44:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e4ee5b0a2ca8a94a73cb7afa032fe69ab6ba3887f9ce279ff3291de3b98a389d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ebdfd19828a9dc8ae471848a060ec7a720590fa9bd02df40700ef0d2e43594`

```dockerfile
```

-	Layers:
	-	`sha256:c5488c334c0a86e4f77f44f02a4340721ae620d69ff61d3a5300978035126de9`  
		Last Modified: Tue, 14 Jan 2025 02:44:56 GMT  
		Size: 7.2 MB (7176182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87cfec1c3d27084b23373adfd60863e908f2cbfe312a936acca80f1af283854`  
		Last Modified: Tue, 14 Jan 2025 02:44:55 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1495-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a7f0726de7935af5d7872c54a9c6c6dbf7a11a5f352e126e8ee989d003f06ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284744171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d13becbe9e3964781abe986e8533e925d2daab94b6f2732492b7bac7a80bfc`
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
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80492bd56138294a3d10e9508d1eae93219173075ed84b75388a4bd08b9cb`  
		Last Modified: Wed, 25 Dec 2024 07:10:26 GMT  
		Size: 155.8 MB (155793105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bc9a1de395d18451f58d37539fa9804524c13b43355c788d4bcd58d9ad4184`  
		Last Modified: Tue, 07 Jan 2025 03:31:24 GMT  
		Size: 80.6 MB (80624545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f57a2d2bddbf7b0361f6b6642bb12fe4ba00db8084975090ffb4a696ea1fc51`  
		Last Modified: Tue, 07 Jan 2025 03:31:22 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aa7b00f95418c3a4cec42fa2bd8f3435d297d7f212ebabe4a11d738289917e`  
		Last Modified: Tue, 07 Jan 2025 03:31:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2768992878489228f9b567eb5af04d4bb89bbff7d886d8bd25bddb8affe035b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e1338a6f545819afe8439cfb1feecc650a21a9bbf2c4e736ebf06190989ded`

```dockerfile
```

-	Layers:
	-	`sha256:5543ff00ee5045cead7437913f990b8f010c8f62d9e4592dfc6b448918580514`  
		Last Modified: Tue, 07 Jan 2025 03:31:22 GMT  
		Size: 7.2 MB (7182017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7d1a9c6454877206dd9e837e8c87e056059c72a9287afbfdf1937b744c6e0af`  
		Last Modified: Tue, 07 Jan 2025 03:31:22 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
