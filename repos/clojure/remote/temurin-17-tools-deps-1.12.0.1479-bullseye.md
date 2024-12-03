## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:815feb0af1fc52e5e10e25beeed6cc704ae963dac3e7117c789087954436c8c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:581eb5e90c3a0fa385ac989aedf87c2bb438848f3249c0ccc2ecb58f5ee89870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267436546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743ef814e76b560689842b4f299762962470e276d0a9fa5501258c2e758e2181`
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
	-	`sha256:f35dd2ce389c2ba8241ab5a1413687a0b57613b16b38bac38a5c7ace5c96bf94`  
		Last Modified: Tue, 03 Dec 2024 03:20:10 GMT  
		Size: 144.5 MB (144536664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e535888fb75f9e22cec1310cd7ba03c139bf3f0f14f1b05264e61fccc15c29b`  
		Last Modified: Tue, 03 Dec 2024 03:20:09 GMT  
		Size: 69.2 MB (69159697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598404607d023cd419afcbfe2a14d8d4710eb9919a0085c41738ed869e2968d4`  
		Last Modified: Tue, 03 Dec 2024 03:20:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537af8a2140187c10455b2bf6297678ed04153a5fd9fecfb3d57909ad09b50ca`  
		Last Modified: Tue, 03 Dec 2024 03:20:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:184c2f0019789827620dc4f5decf74524446cb68b116d6023ae7204f0968ba89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2661e19fe75589c6b1b25570ca53a2a36cfa98ecaeec6a86c7aa524cbe260d`

```dockerfile
```

-	Layers:
	-	`sha256:55e4d2c6d14784f4bb8d29e5a425f83e599877b9a89a796526e665703546be79`  
		Last Modified: Tue, 03 Dec 2024 03:20:08 GMT  
		Size: 7.2 MB (7214067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c906b3c04a8be2bc5ccf9d9ea43a49a63815f94a0e8414a7ba02c3676232d10`  
		Last Modified: Tue, 03 Dec 2024 03:20:08 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fffdd9e45a9bd50274c7d54a24c4eaaab5fea9c9a0a4927184020b12ba00172b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266395520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d66dd106b5a2fca9fa20d840123c4aa14505b165035925dc7450aadbb72ca`
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
	-	`sha256:846c0aadb595ce3dad22540ca4af2a416640bd8bf2e148722e96bb420bc4db90`  
		Last Modified: Sat, 16 Nov 2024 05:30:57 GMT  
		Size: 143.4 MB (143360999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4cb1b100c76f899d6361911741b41c072805ad3bc8f02790d2aea553e8173f`  
		Last Modified: Sat, 16 Nov 2024 05:35:16 GMT  
		Size: 69.3 MB (69276407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb69f1d3047b9c243669b08e512b1a3649c04fd758a3dbb2a339f2eb4c4e168`  
		Last Modified: Sat, 16 Nov 2024 05:35:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bad2bf11153c74f5206a11c815d87be9f64d02f877d62ceddd6bafe2c0bc9eb`  
		Last Modified: Sat, 16 Nov 2024 05:35:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a16f7c65006028580f1f00af2b901768d82edfa7e16cee43a83f941c244c49fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f08f18580b976d30927faede3ce2bd59cc1df44ab72ea5270a8392af8b03b9`

```dockerfile
```

-	Layers:
	-	`sha256:db999ea0887a991ac3617e9299a57c76adccfcbb91658514ea9df1bfd0d953fe`  
		Last Modified: Sat, 16 Nov 2024 05:35:13 GMT  
		Size: 7.2 MB (7220973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ccf7824e6dc1b9df0b663c6e6c626dbb873cdfd2a7a2842396a2554ad7ffc80`  
		Last Modified: Sat, 16 Nov 2024 05:35:13 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
