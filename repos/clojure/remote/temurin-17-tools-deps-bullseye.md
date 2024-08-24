## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:092b6b7ee90be1534735a78e238a17638857dcb64da418a4edee1a38b04ac468
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:89fa4204a92190ebc8dd6b104c8cb2322dbe21a7e40bc2b3e9e7076ea1917658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269214368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c96abd57fb08639810df8c2da6f5de4926970ac504aa37725939053f89b5a29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bada435c6abf18892682e64339c148566831f18dc40ad5858d2cbb6d34c540ec`  
		Last Modified: Fri, 23 Aug 2024 20:02:20 GMT  
		Size: 145.2 MB (145166507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dc73639a1afcf7c3a599e020a2733af3a2cfc4bfadba16f1b4c7d5e6aa50f5`  
		Last Modified: Fri, 23 Aug 2024 20:02:19 GMT  
		Size: 69.0 MB (68962143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e276a7e8dbb20b8593fd9954eb897ed5b528fb19de04f28b71e7577815a2062`  
		Last Modified: Fri, 23 Aug 2024 20:02:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6fe3dd15f3fae6c4e876d65b6acaaeb1258aa9901e3a4ec3e54b06d61b7803`  
		Last Modified: Fri, 23 Aug 2024 20:02:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:21438d38c576fab83096873d5b9170f249fab184a77a185c6445fc0092430b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43705de2a10a81ec8d992a4235b254170807d26235010ce8aece2981d2891a5`

```dockerfile
```

-	Layers:
	-	`sha256:33cc259caaf75867a7c15b7ca31d10872e8e99cdb635cdd9f65c155ec58640ca`  
		Last Modified: Fri, 23 Aug 2024 20:02:18 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f671dc435bed783d880a5ea0214fa4cf875dc4c6416f7e82b3ddc83b23c63665`  
		Last Modified: Fri, 23 Aug 2024 20:02:18 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43c6622a59b0eb52d525ce7657f514791cbcbc6ba1d232cd667b605f25490b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266783752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc084f17ae03249aed837f65450dfc0c93b8d262030dce523729d317cb89e3e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d3fde3d3d17b93a446a4eecbcfa1ebd2d2f9f07d55e44c654e037142ffeade`  
		Last Modified: Sat, 17 Aug 2024 06:13:14 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77521bd76333abfad2a96b2f337c87aa69c3a370a49d4bad54ada06969cb108`  
		Last Modified: Sat, 17 Aug 2024 06:18:15 GMT  
		Size: 69.1 MB (69093317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0f3fc0f29d1cc9625c614d4a1156da3185f41c724ca7f82634dcfc3813d6a0`  
		Last Modified: Sat, 17 Aug 2024 06:18:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fb47b218c2eebce60e19bc8870d6b5748c056836f5fa767ab8b3a82cb1e6ed`  
		Last Modified: Sat, 17 Aug 2024 06:18:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:edc77e7b78d7c1ef0f7b2dc4ed5894f4bffb5101f2e5041270538cd887488c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6c1fc47f993675a0733758cc200352115ac234338d006cf537da39abfd1d69`

```dockerfile
```

-	Layers:
	-	`sha256:66cc7096103c93a4c3de25efb443ab9221fff67d0a44f9c9d674a0e7cc6dac8b`  
		Last Modified: Sat, 17 Aug 2024 06:18:13 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdca6e0d810597cccc63ec6dfb1336905aef9fc4cafa091f4442f4582d70fa3e`  
		Last Modified: Sat, 17 Aug 2024 06:18:13 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
