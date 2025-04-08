## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:b3206f019190855c73703412b941ad548d8119047273804c373bc7155e844c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5be8ca0e44f0209aaa9ce53462dade38636de82a386a1da803421b0e03723339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267710984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbd7a8c59a62b63ce1041d1171c977996cd3f44bbb1f78e353f10215e4c5f2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384928da5074ebbb01e61be8084d664629974b9f4e2c65abbf0cbad3448967e1`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 144.6 MB (144566556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a7b9df872f183423f2c4b5d6ce0e9134e9cf585d55f20e3d004184cf16505`  
		Last Modified: Tue, 08 Apr 2025 01:36:26 GMT  
		Size: 69.4 MB (69394861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dc9a660bf5d24c6933fe2c1ab81ab3865c29b3dc71d8b38a365fb5e8c234`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dace952059d21a364d77d6f9caeb22fd94809b7bcdf8fb098883ee51b17143df`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ac2cfcc388ac2e3a533cf27b960380b839b7a0d1bfb93f4c8f6b9b48f19dc810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1df5e31158cdd29ebdb5129ff5e6d6819d430b131062fa65a2c18ae7d9575a`

```dockerfile
```

-	Layers:
	-	`sha256:e9c0edcd820a05641f5c509f0c0c6b7ad488b956ca1bfcb2a0427ddc2ae6dad6`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 7.2 MB (7206501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c54040f0735796fbc8cb3fee9f7a3c6fe8e42465842a4f811b016b12967a9eb8`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eea80442ff5d10a2dfb1d00b92f4bb59ca13ed9a633407f63a0932323912e644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265239557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20685ec849506659bb9ebf993658cb4333c2c330182984f8360c731ae26ce4d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b78c9a7099b2ef01571f7d5b8b18d1fb930e46001fa81052be0bea3123bdfdf`  
		Last Modified: Tue, 08 Apr 2025 11:27:21 GMT  
		Size: 143.5 MB (143454701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca10eb03135f69bc07f848aab81855cfe2e8e5606d3682ada89057abc48662a8`  
		Last Modified: Tue, 08 Apr 2025 11:30:19 GMT  
		Size: 69.5 MB (69529591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9a033b46c4586d25beccf5af93fa2d4ffb84631bec3b63855197b79910cfdb`  
		Last Modified: Tue, 08 Apr 2025 11:30:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586311341a03374716532bf3c8629c5e1ca2acc95319504539475cd5de61bd0a`  
		Last Modified: Tue, 08 Apr 2025 11:30:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d144cd8389a05fae26d6036b3fdfccf50f2886c2cb381f9be3b5af9009891e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86aabae43f6ef334d9fd16a2d4af9fe7c93d3c2f789eafc57d1683ec0f21233`

```dockerfile
```

-	Layers:
	-	`sha256:71d3951b402603a975dcb139602838e27c7c477ef2e546b060841b480558b527`  
		Last Modified: Tue, 08 Apr 2025 11:30:17 GMT  
		Size: 7.2 MB (7211600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883f53f29b048d3a28e2742d8429bf22e569b52c4666ec4975efc26c05cbf4d7`  
		Last Modified: Tue, 08 Apr 2025 11:30:17 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
