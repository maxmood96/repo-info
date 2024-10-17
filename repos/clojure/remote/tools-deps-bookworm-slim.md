## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:eae456b9ba3a5dd4eebc0990b7348848562a078ab29fbfd13ab9cb28210e610d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ec18f8058fdbea1d5562379198e60b0a0007758d92dcc5f126d4661955ba5a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257189328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262d4f99296af85ee6637e0e3f4fad7d23ce14f686f158ac6b4fdcac27674ef8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9a55bedeb6594dfbf1d53f6c70952965a0fa5b1354b840d324a0d580574e7f`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 158.6 MB (158579244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50313744fc8b2c3ec4e370b07841941b1e7f1468f7ddde8407ef1229dadf0be8`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 69.5 MB (69482756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92407d52db567e1f8bb17158ffa0831c4b0f31d244c64032486ca89c05b7566`  
		Last Modified: Thu, 17 Oct 2024 01:13:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f957a6966887b2286056ba5dda9b3ab3c5d32fbddc0bdb166332c05d147aae55`  
		Last Modified: Thu, 17 Oct 2024 01:13:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:68ced2d865c365810d5c238a5f734c0fc2b35ea5a2fe7b64cc54dcbd8dd9a075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4914895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4aab829e44a82164adab3c9f5d9e9b5edd35adbf2ce7cd1cc1706c5009a89c`

```dockerfile
```

-	Layers:
	-	`sha256:3426590ba09cf13cda0e1926f3d73b78d24b03a932a814acf589e4e0661c1dbe`  
		Last Modified: Thu, 17 Oct 2024 01:13:37 GMT  
		Size: 4.9 MB (4898648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcdce21049005047813152d6ee0bb401b306a00acebc98ee02a07e7b4191655e`  
		Last Modified: Thu, 17 Oct 2024 01:13:37 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de29140e296fb22c8598f5699f7cc08e2e378df6663ba06e332492ac6270b13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255248907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704efd9fc292d1203235315705a116c0396a386c20137a863554fc8f6796bea2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c16ef64a611abb0917203f086cab4426e687c1c31700d511fdb759b51538f86`  
		Last Modified: Thu, 17 Oct 2024 08:20:06 GMT  
		Size: 156.7 MB (156746200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159627b69b998cff9585a6578c6067800a37c62467796aceb2c93e4f518a0097`  
		Last Modified: Thu, 17 Oct 2024 08:23:55 GMT  
		Size: 69.3 MB (69345327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fae276bf5794fefeb7d7f49a1839cbd5f077eb84d9b6ca9af597f80b869817`  
		Last Modified: Thu, 17 Oct 2024 08:23:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77b2634f2cf8fb6b84e98b2d36a94696d19fd4bd8be8732895d5443c13e3fb`  
		Last Modified: Thu, 17 Oct 2024 08:23:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:440993ca474c6f93cf1b37b4bf5ddd2445c411422a97464e52dac4ee77322385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db962a68690b26f2dcc63feb9c463fdd83ff5e15a8dcf862a91cad6ce4f6236`

```dockerfile
```

-	Layers:
	-	`sha256:8010bbc3a540232f5bf51a372cc5a2acdc3b6fd783f028d82a5d3769735547a5`  
		Last Modified: Thu, 17 Oct 2024 08:23:53 GMT  
		Size: 4.9 MB (4904438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6622694192cdae9a3f32741d46de4596d159794f5dfe9a04152b4bf19581b310`  
		Last Modified: Thu, 17 Oct 2024 08:23:53 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json
