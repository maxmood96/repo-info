## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:a5f960125f2151cabf512fddd2959da5a6b5615ddfa0adaa83d7ca3ca35dec56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:72cb5f159af5d638fbdd981e72af7566bfedafc1784089e221bb956ec958f9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262820800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606cc154007304811d8fdf5e7f435e7e3c87ad0d637352e4ecc298c45ba51e31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb59a3d9e55d5a8eca495bcb097361d50f4ebdc8dcc8533f146a6b2011a6a49`  
		Last Modified: Tue, 03 Dec 2024 03:26:05 GMT  
		Size: 165.3 MB (165295086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987338f6bbedc5a744be7eca2f94fc220ed1a1c3695457e20ef15f02d1911596`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 69.3 MB (69293094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795787dde72fa19b001d6da7a74b02081d66da6ebc6b6690020de7df20897a9a`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd248d1244758eb79218edaf74e29b6635c3e80739deeb95601a9fe5de6c476`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ea95dba04640a97e8c0953983162cc02c9ef0a7533e42a735dc59d4c677c453f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d015ec026d29cdc462b14e081ca4db69776e2e687c691eaee0114e2bc3ed78`

```dockerfile
```

-	Layers:
	-	`sha256:39d548795b8367eb343724073ce076cffa95bd21a901d4c72660e36199bf4c68`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 4.9 MB (4924393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae75e2e8eb6be9533a6616920161baa4f5970abb13a65d0d1c83196f5adb27c`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acc7c3f36382ac12c0ce0498a72d245e35666a64f7486ab4ea21c50f872f5bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260482715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771b0501c22b9ed9187ecc2ddb0e5373635f0472e7a340d0accde5facd8b4d11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982780e928391e952f0145329b70cf65022247473d929b5421291c274f82ef8`  
		Last Modified: Tue, 03 Dec 2024 15:33:09 GMT  
		Size: 163.3 MB (163281795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a88f5ac7f037f635af83b79502093754de00b45ebdb115ea3f415608d5aee67`  
		Last Modified: Tue, 03 Dec 2024 15:37:24 GMT  
		Size: 69.1 MB (69141068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9dad40b02f0e75835dfc4089b5816c137b97d5ecd9d7c775557a05d06bce86`  
		Last Modified: Tue, 03 Dec 2024 15:37:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc329d98a0d9c16ae728466a0401ed9a0ead5cf78062f97bd098dea7545da`  
		Last Modified: Tue, 03 Dec 2024 15:37:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef7abbab89fafe5a52a2bd9741b0ee103f3984f30c4b50ccc826804c175745fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa6b53f8caedeb2e9dfef31327c5f2c0760b3991c0b2ffece4f87064d6f987a`

```dockerfile
```

-	Layers:
	-	`sha256:68f86399b37474f9ed327dd881454719beab40ffe36437c16d4789aab43de138`  
		Last Modified: Tue, 03 Dec 2024 15:37:23 GMT  
		Size: 4.9 MB (4929537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b437ebe2e51709a57cd09200cf2cf28dd61e79c9d2a7fd24530bea4fe3849a`  
		Last Modified: Tue, 03 Dec 2024 15:37:22 GMT  
		Size: 16.0 KB (15995 bytes)  
		MIME: application/vnd.in-toto+json
