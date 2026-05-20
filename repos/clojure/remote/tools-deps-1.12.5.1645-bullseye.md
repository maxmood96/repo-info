## `clojure:tools-deps-1.12.5.1645-bullseye`

```console
$ docker pull clojure@sha256:9b79e4a223bf521e616e419d59629a60e6c31c9d0546fb1969672d001e0ee0ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.5.1645-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:14460b78c7b357af82f135a30572897289deb7b6b62cd938aa81d54b76dcff09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215946569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5415322a7182c75c4392de91fa77e39b9e75ab296c878335f29a847190b065`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:01:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:27 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:01:27 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:01:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:01:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f5421f81c25644d3d14d116a9fc3f3e333d1c71464cad459ddc17fa9030b3d`  
		Last Modified: Wed, 20 May 2026 00:02:04 GMT  
		Size: 92.6 MB (92574585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbe345057836aaed58fa019507e970775520bc5de0b4e73063d00bbccf624af`  
		Last Modified: Wed, 20 May 2026 00:02:03 GMT  
		Size: 69.6 MB (69602093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f325e16bafab68de06974f048347906dbe4ebdfc63aee44c1bb36728c586a32`  
		Last Modified: Wed, 20 May 2026 00:02:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feaa326056f210d385b4d3468e2d006ab60b24c56bfcd08a0e83599230b8fa5`  
		Last Modified: Wed, 20 May 2026 00:02:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5d906ce73f383f0b644c25e765e693e2cc0e8457c20212d749288aca6d78b0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e3bfe4411f8d265c5bc0dcb06b24735a9db3e4abd7579085154f5695893f42`

```dockerfile
```

-	Layers:
	-	`sha256:fef546067758cb6747df17a9568a5cde571f25d6b96f4521b8da879da982750d`  
		Last Modified: Wed, 20 May 2026 00:02:01 GMT  
		Size: 7.4 MB (7376348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0265be79a6a1eaaa2d36180e3d4417057b94b1582a5ef5a04afbef0f85a6b941`  
		Last Modified: Wed, 20 May 2026 00:02:00 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8f787b680cfdc431347c94fcf3e274cb379389c8442d220e304817e9131bd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213570809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3b68e34a0d81fd5f31327ebcd0b9a75582fb528a87cf6fe2037ffac2020b51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:13 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:08:13 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:08:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:08:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f54d3633b08ed277ed9834ac7ab4097024d9a58782d5e5e75188beeb3adf4a`  
		Last Modified: Wed, 20 May 2026 00:08:47 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090d46046fe6ffea91b6168f1e9f431d70bad556ffd434109b74b12bf6035a13`  
		Last Modified: Wed, 20 May 2026 00:08:47 GMT  
		Size: 69.8 MB (69770936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affeff61e1e517c6ad9a9f5103b8099f0d7dad6894561bf8bc25f3b7e9cdbce5`  
		Last Modified: Wed, 20 May 2026 00:08:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20a671a7956200fd9e6a3e33e626e201f98cc0c695d43f5b236b6e3b8e5e9c9`  
		Last Modified: Wed, 20 May 2026 00:08:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:779b02da6c985701d0b3b5525b9c958bd6362fa6c28b6dc07f83120ec0a0614a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f844307c08fabd359921fdb3f82409589eaa5122023e9f7974944fc79eec535d`

```dockerfile
```

-	Layers:
	-	`sha256:414a72c0e3864f099a24ddc3c601ed5c6f2e63ba5825f4ccd93d4545f12a8cee`  
		Last Modified: Wed, 20 May 2026 00:08:44 GMT  
		Size: 7.4 MB (7381468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51561d60aeea17ca82aa25ee1bea27189da11bc9fff92df94cac87f5b657ffbb`  
		Last Modified: Wed, 20 May 2026 00:08:44 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
