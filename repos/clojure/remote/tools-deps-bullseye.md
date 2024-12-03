## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:674e09932d512f9896b15526f8386f7528b23f992e74caa44cf93ebf8d8293ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e6d81a5c92d96f2fdfda666323df58124d5f7960e531382fe0ad543ef4b39e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280468467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe1f1913a22228a05ecb7d9342ae6b5bd6abdd43db49867bcbbdb16963f8e95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e90cf8378535604d9938b186be006972adeec072abf069c1ea8f34b1cc3bee`  
		Last Modified: Tue, 03 Dec 2024 03:25:56 GMT  
		Size: 157.6 MB (157568687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5442ef7ed80dbc8dc6b7e7ca74395aef040fe0b0902c55f07edec1a3835572`  
		Last Modified: Tue, 03 Dec 2024 03:25:53 GMT  
		Size: 69.2 MB (69159595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f910aa5e37e8276cf05c596787837807e448dcab69c81ac6c51d23aa6191e1`  
		Last Modified: Tue, 03 Dec 2024 03:25:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206e3223f9ff779b96fbaaf2172b6353884a812ef636a8452c9421cc18df3875`  
		Last Modified: Tue, 03 Dec 2024 03:25:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cb5e7fdf6056e487123c84b6af91c9f73dbc79abc01f7ca2f99424f70d8fa926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aa3c4aae2a84122daedc4c81ecaecf824ce82dd3f80692ebd713a365ccb70f`

```dockerfile
```

-	Layers:
	-	`sha256:a23d4bf300fecdf912ea66f34c747a1e9b7722e47ca06405d68de32bfc1e6d4b`  
		Last Modified: Tue, 03 Dec 2024 03:25:53 GMT  
		Size: 7.2 MB (7217850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def7ed0d654e8650af7b3a31b54185e19d257074bd93d4cdae48048cfa43f96a`  
		Last Modified: Tue, 03 Dec 2024 03:25:53 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a29fc9b6d3c56e779802dcf4421bc32f88ac47827507ee909a9029c0d48956ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278827455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be636bc23da1da77e61b152c5e9149d33d1e208f1d82b75a1412d8513f32547e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe2fc906056795db59cbbec672365f3ce425ed8a02c6b0a2bf0d4e922caf66c`  
		Last Modified: Sat, 16 Nov 2024 05:39:29 GMT  
		Size: 155.8 MB (155793109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f863c5a54ada89eb751061bae338acceb5ac8a32cea67826daf623c05d79eea`  
		Last Modified: Sat, 16 Nov 2024 05:43:56 GMT  
		Size: 69.3 MB (69276232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d38eb27871864bb3c00089fcec256bbb0dd42c8d374c6695a02ee040ee9ef`  
		Last Modified: Sat, 16 Nov 2024 05:43:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c267ae9a40f45e04bd77bc541420693cd1b616adea22af1defa7cc8f4e8c6`  
		Last Modified: Sat, 16 Nov 2024 05:43:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b342ca4e6755645ed8d9e1de95310b107b20e0f343cae34669b4b606b14ee681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38e4de4ae89287d0d454bba52ed38d324cde0629c7fab75287ecd5f709a8ee8`

```dockerfile
```

-	Layers:
	-	`sha256:38361d3a1d97eb33e9da5c720a7390f6d13d4d1c4cc9257c35688ac29142b64b`  
		Last Modified: Sat, 16 Nov 2024 05:43:54 GMT  
		Size: 7.2 MB (7224780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cd780d3c71183df9a60f760fb81f52997d14343c1eb8e42224387f414571f0`  
		Last Modified: Sat, 16 Nov 2024 05:43:53 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
