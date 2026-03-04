## `clojure:temurin-8-tools-deps-1.12.4.1612-trixie-slim`

```console
$ docker pull clojure@sha256:7558c7aff026daa302c1a0016b4f83882c532b3d96f33ddd4b1a08ded876254c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:63ebfb37784d4e2b2befbd868c0828da3cab2731dc23e0a4abd6b9e17591d21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156964060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0faa5c8e133d9eec6e46e722a0edac927f0efb016d414a5d96eecf77a8a7543`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:07 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:07 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb11eaab09dded8809201afb10a0e0e96ac1251135ae4690c915ed264f43d5a9`  
		Last Modified: Wed, 04 Mar 2026 17:49:39 GMT  
		Size: 55.2 MB (55170059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2473be22a6858b046169701c68f5e699e89522ad8972ca84eb556b0a9608124`  
		Last Modified: Wed, 04 Mar 2026 17:49:39 GMT  
		Size: 72.0 MB (72014724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e671f5a0f90f01590c00c9e6dac578c04b6951459fb44885f707974453308`  
		Last Modified: Wed, 04 Mar 2026 17:49:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee2741c48409c415ad60fd66c9368d20094a5ecab76026de32ea4bde32957815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097a07ba2f92fc12ba65997bcd900293ffab7457b8e42f99942a543509c58122`

```dockerfile
```

-	Layers:
	-	`sha256:af2004cec4468b74e00402641c52c5cddb7962e691dc6ea92b3ab2bdbf43baee`  
		Last Modified: Wed, 04 Mar 2026 17:49:37 GMT  
		Size: 5.4 MB (5380051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcb9f104f0907614dd40e5ca2125dbe00b6d5c1e8aadc226437cdd0d630ff4b`  
		Last Modified: Wed, 04 Mar 2026 17:49:36 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:93ed1dabde6412eddf034124cedd9ad9cb218fccadccf6c65b201ca245d24e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156223738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bae975946c69048936b89a8baae3483cb8ed866316c23c974d0c2b6fb704e43`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:48:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:48 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:48 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb4fed75e276b0c038c2f8c3d825a2d3b4d630b627d580d1c32a9639338c408`  
		Last Modified: Wed, 04 Mar 2026 17:49:24 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab51368b5be285b8d04a3288614aa257afb3a63e336f76afd292bdb9032c7bd`  
		Last Modified: Wed, 04 Mar 2026 17:49:24 GMT  
		Size: 71.8 MB (71831380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8430a45ad65cffc9a0bf0401f67d13c4e4770aa366115fae51f206d52b633eba`  
		Last Modified: Wed, 04 Mar 2026 17:49:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5407ba4f4a9b50d326bc662fe76f583992b6d8e0c20bf1f9d3b654c56093e536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceace2c596a0b0d4ff38f54105ad966e3d7a08e5c9f65188132839bf4c180e2e`

```dockerfile
```

-	Layers:
	-	`sha256:9cac849abb7e0cac11f0d1faabf1611e21348c1983fd84f9d48b412d6d9d7eee`  
		Last Modified: Wed, 04 Mar 2026 17:49:22 GMT  
		Size: 5.4 MB (5386520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75af477e7e58bf48971e29eb104146ab663e166b5d439b0895113aea088f48f5`  
		Last Modified: Wed, 04 Mar 2026 17:49:21 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:08883f6f2a9ca84ba2d001e9cf960b73b918ab47b448da0d385e25148e0fc1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163679591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97baaf46d907d4c95aa67ec377ee08b5b9fc850358b462fa2ae5be7a6e7b5c6a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:33 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:34 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:52:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:52:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:52:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a9c95c6268eb99bd413b7321a4cc160d25b3b24cca1b72721e3fd239d13e0`  
		Last Modified: Wed, 04 Mar 2026 17:52:58 GMT  
		Size: 52.7 MB (52650390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808e3895647d78b33f1d247ba944ed7488eb19734543c20930bb65972f1cd78`  
		Last Modified: Wed, 04 Mar 2026 17:52:59 GMT  
		Size: 77.4 MB (77428337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c0605e3baf2c174b908af944cc6cffc121944b8a08f02a3db01c03c838a6ea`  
		Last Modified: Wed, 04 Mar 2026 17:52:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05225b8fcb58965f70b3f34a58e449acfc1a8f4286a2b05bf11f30f5bab94084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ffb45ce002085bfc1ef8c18b48ea6ffc11d64c036ebf27bbf973367fa3baf`

```dockerfile
```

-	Layers:
	-	`sha256:6411a68484eb9335815d01d45315e71f823e39fee070ab77fa6e13ab29cc1b5a`  
		Last Modified: Wed, 04 Mar 2026 17:52:56 GMT  
		Size: 5.4 MB (5385017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c5db4301a80f689ad7ea35c8feb9d4788de0f2c6b95dd4ad5706fd6ccd98a4`  
		Last Modified: Wed, 04 Mar 2026 17:52:56 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json
