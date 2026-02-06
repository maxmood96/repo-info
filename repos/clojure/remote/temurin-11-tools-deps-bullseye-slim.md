## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:89425a0d4cf5c730ad0ef455191f0e361bb386624e48d91b4aa76bc4b9b95641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8353c4dbadfb67be4b63d0e23bd237fad6b840f58622a79c76f84a6bb277a295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235202523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9ed541bac9ab12aa369693ae5fc6ecb48e27bce59102dcff4c2fa6c73b4bbd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 22:50:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:50:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:50:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:50:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:59 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:03:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:03:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d32210675fee0f3d85ec1b09926eef061a155419967296aabc3c9bd9d83bbfc`  
		Last Modified: Thu, 05 Feb 2026 22:51:23 GMT  
		Size: 145.8 MB (145806917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e567a4c3e32499f89cfd5444ba61f9883418401fac43f4369302eafded2f48`  
		Last Modified: Thu, 05 Feb 2026 23:03:28 GMT  
		Size: 59.1 MB (59136675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33425ebe2923bbb441b95ec183d484ac18ab0bb15321823a17e6c40fc31cdf8`  
		Last Modified: Thu, 05 Feb 2026 23:03:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e7fe4e75ca12b7b9a800a65b20930faaa94eed9b3ca31ec211a8dcb48c6dcfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3798daec73136670f91d8316597410a18f43cc87e4332bde29ae75a06e6b027`

```dockerfile
```

-	Layers:
	-	`sha256:fa90ee0a3d7b06583fa63b17ebfd4af9de5589f94d02aa792c00dd7ae1687ed7`  
		Last Modified: Thu, 05 Feb 2026 23:03:27 GMT  
		Size: 5.3 MB (5330261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89cfba0e6dca6096b70ccaf32a3f3dc4ad8ed6b224cecc6626758fe1f28a792`  
		Last Modified: Thu, 05 Feb 2026 23:03:26 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:14274865fd16849d035a67984175d20dd1f3737ea632bffb198dafe5ccebbed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230533981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf73dbd59c81c0e8baaf0e861b5a50c147f66ae7ec1228c552e6e5e893dd949`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:04:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:17 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7a61c278f57cd37b71b78c766e77886d81b0b3d2d9f31104c2558e25aed662`  
		Last Modified: Thu, 05 Feb 2026 23:04:54 GMT  
		Size: 142.5 MB (142500855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfefb91e89dc90c074356dc758b3a0e1b090f468b538814683f0e061783c8388`  
		Last Modified: Thu, 05 Feb 2026 23:04:52 GMT  
		Size: 59.3 MB (59288042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3611dce9cedade5a270db0179fecce7ceb51a48b506da7be50da1a703ac88`  
		Last Modified: Thu, 05 Feb 2026 23:04:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3e26fcbbee99ca994926fd91bb1e35baa08bb2f9475c6ebf5c7eb6e473a1f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f8b246be8943f428436150cdd8ab8fb28a88e44f578a6448dd001e0f1d6b11`

```dockerfile
```

-	Layers:
	-	`sha256:12ad56b692c1d1f38ccbd21c434fa98dd8c3c4ca9ce4423fb55f665311d80a86`  
		Last Modified: Thu, 05 Feb 2026 23:04:50 GMT  
		Size: 5.3 MB (5336611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44abcf0bf29c02e576c654230112ddb2a2e071f7ba917f7f94dd676e9bbcbe3`  
		Last Modified: Thu, 05 Feb 2026 23:04:50 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
