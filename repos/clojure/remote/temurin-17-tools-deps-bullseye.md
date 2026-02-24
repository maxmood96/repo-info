## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:9f335197f5acc82f3d56bdd5c5f8851ce74b35469967f024a0c73e661a623e96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fbab1d2ae681e4a6413032591608271014251fd18652dd2c317aa1b47e830c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268954200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe10081fa08b50a52cf400112ba538bba4927433cd33986cf26ef4bd4e2cb76`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:55:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:06 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:55:06 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3b066e7e830f523f95e48296830c58617460914d7d4ee670af36ba84c31d10`  
		Last Modified: Tue, 24 Feb 2026 19:55:41 GMT  
		Size: 145.6 MB (145628702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf116a31dbc704b999c036a301e7e27a5460d42a65255cfeea8649d01bc9672a`  
		Last Modified: Tue, 24 Feb 2026 19:55:39 GMT  
		Size: 69.6 MB (69568026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26671d22bc4484ebe35dcc15049c692029874a99eb4069fbc989ca85ea59028b`  
		Last Modified: Tue, 24 Feb 2026 19:55:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6509962065d50ac8db121d650cf83f62319c77820dee575d90de6dfb11cad9d7`  
		Last Modified: Tue, 24 Feb 2026 19:55:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8a08a6060c405623a62134268fdcfd7d4027848fdcde26eb448dc0aa407b1091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4f8ca97780c9334fa38d8e136a1a991103e50e8381438ac4a39a0e3ba76eff`

```dockerfile
```

-	Layers:
	-	`sha256:15feac18608246a8bc296467e03e5e68ad9b93df515dff2b66836a7b1b33a03d`  
		Last Modified: Tue, 24 Feb 2026 19:55:36 GMT  
		Size: 7.4 MB (7407764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4495541041f39d1a01ebf8d6612a460817988236580803a0a96aa2e55c216009`  
		Last Modified: Tue, 24 Feb 2026 19:55:36 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26e72cf18a733e06f370c7d02a0232e405ac37e664c778e6cc2ffbd8328943be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266403705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3417430f49dd2ad45daa58a9980528e50b43e730cad5754271d6b80d4188102b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:06:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:06:00 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0287c0bf54af45b662af9dfa8b084622e3a3fa8fe26719feeca0913c2807589`  
		Last Modified: Tue, 24 Feb 2026 20:06:42 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224c77f2e2f74dd3d7e208e6d3094ad736e8587817f1d61444508ad61055fec5`  
		Last Modified: Tue, 24 Feb 2026 20:06:41 GMT  
		Size: 69.7 MB (69708072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9762afadfbfa6caad4904e7e73d5692fdb83a2c23acb5e7d1e5b4a56a1510e0b`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b7eb39915685997d8cb8457a24ed32dcccf96f039e18f74951a38dd8980c80`  
		Last Modified: Tue, 24 Feb 2026 20:06:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:858fc7602cd5378a02a842aa037112586dd5282bc195dc177ace4f1681f5f1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fae3c8481344a6e1c94cf795e69ad8d28ae499b1247d1f3aebfce1ec552a3b`

```dockerfile
```

-	Layers:
	-	`sha256:c67d727ee9993beddf9edc6b1b476149749aacbe8ce6cf443ff950f4ff59a1eb`  
		Last Modified: Tue, 24 Feb 2026 20:06:38 GMT  
		Size: 7.4 MB (7412863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db24bc8c5075ef833ad4e80ee1dfe7102fefc9964f9fca741bd8c6affd2b1e08`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
