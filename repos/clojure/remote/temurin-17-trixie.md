## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:72537a2b26342a3d0a6eda68101142bc321e7a4318d50f5c0ff3fee047a5857d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1ba3fee8017a15cf496cb2bca277734edd528fe3314dfb570c76360f9edb7cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277742836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bdc7197d81d25ca5ad76b93976fb4c6bdf372bbd1879f70d01056335063595`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:18:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:18:59 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:19:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:19:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c373b83d73250ff7435589f16faf985a827de56fc766180e3aeb35902caf64e`  
		Last Modified: Thu, 11 Jun 2026 01:19:43 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d388d9e26ae9f16414e452a88234894930bb012601615bd184a190c551d2e1b`  
		Last Modified: Thu, 11 Jun 2026 01:19:42 GMT  
		Size: 82.5 MB (82519218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd2dba655acbe122e79028166f472a0999dddbc6b8981ec6f902a398ff522b`  
		Last Modified: Thu, 11 Jun 2026 01:19:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648314e092c529ec628177818f8b2cdb66480266a44d1d882512a298414dd8bc`  
		Last Modified: Thu, 11 Jun 2026 01:19:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:966f978a29f6240f75785245687783c4b9011a2b74b4660c2d4eb58bffc1fd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4eca9f9fdf3b7ad8f19473fe57d3b32d95d24e5c6a60775a8084e1a815f38c`

```dockerfile
```

-	Layers:
	-	`sha256:0d310f07f5f72b3bf4f9fb88b436e123600a7a0db03c62f3ac84d156e83f8cb1`  
		Last Modified: Thu, 11 Jun 2026 01:19:39 GMT  
		Size: 7.5 MB (7468771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729c9642850481d589490f3de3083d24646f1cb097fddea6d99e38a83754bb41`  
		Last Modified: Thu, 11 Jun 2026 01:19:38 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:197d9a669df3ea0b037cc101a04a7865b772390a61b24fd70610c13a53505e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276742115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3d4c8756a71494d8d6cd457aace9bf3dd71bbd1283cd218fb7f7bcf62d5a03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:23:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:04 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:23:04 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:23:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:23:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90df94a45ce8cdf8943626da8ad7c924e9d00cf99b6f131ff06ce5930edd5382`  
		Last Modified: Thu, 11 Jun 2026 01:23:44 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe741b5609d75a007a79f1c35c6b8ae12145d940ac1dc19e549d124a1a9742`  
		Last Modified: Thu, 11 Jun 2026 01:23:43 GMT  
		Size: 82.3 MB (82338545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eef7b982c3a2f999d4418c89f20c47076610c7faadadc9752d84c79d4f753ef`  
		Last Modified: Thu, 11 Jun 2026 01:23:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8150c6a9f05c558a00bdb9c51dcda37fbcde7d3788e99463b31ed5b4ae401`  
		Last Modified: Thu, 11 Jun 2026 01:23:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e2207c342885d221d2694425c9dff75d1ef3cdab8b2eaaebefa7d9f53b3abcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c191be876d999e747377dd25343ba6bb3d8b8935c36895cec6f7af89d6f4ced9`

```dockerfile
```

-	Layers:
	-	`sha256:4eccd8e1ac715a1715b81d3e230c020cb9f7f261b54caafe83b339c0894f14f0`  
		Last Modified: Thu, 11 Jun 2026 01:23:40 GMT  
		Size: 7.5 MB (7475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af6ec82a92fef9c953679cb39c4a7907cc1a5ec3e81442ab1a0d796b0601b09`  
		Last Modified: Thu, 11 Jun 2026 01:23:39 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1f85f7feee0716759d34c4d5761893004b3318f8e053b45637e76ad2b8ee6dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286837281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177265d54ad4997a34db50b65401e07cd6398b7235c333cde2596e3126047c0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:56:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:56:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:56:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:56:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:56:04 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:57:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:57:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00b56959c90c5f0fe14cf07141a8ccbb5fba2b1e9b43bac05ab20bc6c254eda`  
		Last Modified: Thu, 04 Jun 2026 17:57:46 GMT  
		Size: 145.8 MB (145766113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ebb907f06aacca3fd75882735b8ecd5cb02a297fa4ae79c61549ef21448bf`  
		Last Modified: Thu, 04 Jun 2026 17:57:47 GMT  
		Size: 87.9 MB (87937944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439bbc873207caa070ef845e8e407f52fb17ca10c30fea691427417c15625631`  
		Last Modified: Thu, 04 Jun 2026 17:57:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bbb08d21dd966fd6d86549437031ed6ed2a92bf68fe01aaf2e782931823ef0`  
		Last Modified: Thu, 04 Jun 2026 17:57:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:52da1908f5cfcafd0df49b6fc126039e454dc1906a07520fbbb39e690df8e0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaa31a917e61511cd1a61efbaf3331d83a8934e024bd68abd9e6f8cf5e4488f`

```dockerfile
```

-	Layers:
	-	`sha256:5dcb4903615f5d49b98472525e698c9422728d5a931c876f46451cf880216e1b`  
		Last Modified: Thu, 04 Jun 2026 17:57:44 GMT  
		Size: 7.5 MB (7473192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c80e0d00023918519eb0a12bd1b9d890f1479548241b9ba7417e54abb6bbf85`  
		Last Modified: Thu, 04 Jun 2026 17:57:43 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:66e1e9353d00953a93187599fdc68aa70608e98579eb1fd6ddf62e09fadf9d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268799319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d032491f9ab768c3936ef6720d5e8e17ddfbf0db8f38a46cbc4db5f7e15eb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:09:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:09:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:09:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:09:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:09:10 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:10:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:10:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:10:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:10:29 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:10:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a727f4eff59ad89139dcf74c95cce8838b028ff8c9fba9099a34d7f75c8ce93a`  
		Last Modified: Thu, 11 Jun 2026 03:09:51 GMT  
		Size: 135.9 MB (135910421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee7aa18f0ff800d794a5f5048ccee8f6a2673a5d1958b7841f5f6ebbe67f4cf`  
		Last Modified: Thu, 11 Jun 2026 03:10:55 GMT  
		Size: 83.5 MB (83501963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704dfdff5bb9e5db5c4e0672bc64921bb5833a6b9d5213eb0e6d994bb4353d04`  
		Last Modified: Thu, 11 Jun 2026 03:10:54 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98953b734dc98dbc6be2f604129eafd1a2871abadad4477daf4c6ab984be9c9d`  
		Last Modified: Thu, 11 Jun 2026 03:10:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:56c446a5fb8c2c298db71082fd92429a7dd324b1d3dae0ee93a5ce61a07fb938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed5f9719bce445c3c38cb4798575fc3fdc17714f229f9219a483544b114471c`

```dockerfile
```

-	Layers:
	-	`sha256:dfe6026d28b8054e46b62d839c11fe14ea80e2c69d2b626070a5cd43837dc4e0`  
		Last Modified: Thu, 11 Jun 2026 03:10:54 GMT  
		Size: 7.5 MB (7464693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7770d9db9e8886ecd886afaabaa3ddfa503b2ad7d9ee3ee657afc4fcaa25d49`  
		Last Modified: Thu, 11 Jun 2026 03:10:54 GMT  
		Size: 15.0 KB (14953 bytes)  
		MIME: application/vnd.in-toto+json
