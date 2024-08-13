## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:139d929ce1af742c606fbc465f418def5013d442ea86ae556be61a0f5a51811c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7823562bab8cbaa66b3fa0d8778559f1ab1338963b4017560885394f6f1e8213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269214751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebab64018c049b8a92c4022142e8d1c2dc3b3e590759760bb79637c7f244a5ab`
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
	-	`sha256:f769d58d89eb3b4263480c02b2dd20bbd26f5169672719006e069dec4266da71`  
		Last Modified: Tue, 13 Aug 2024 01:11:25 GMT  
		Size: 145.2 MB (145166531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899769a10bf056b72347c86c0e7beb6e0566f76c22c0f210e29773704cba1c23`  
		Last Modified: Tue, 13 Aug 2024 01:11:24 GMT  
		Size: 69.0 MB (68962505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cecd8cf58605d5466a4d686ffe8aed7e6ad16c93fb0a24c7887569c38bd6a93`  
		Last Modified: Tue, 13 Aug 2024 01:11:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d296d91b65fbb4490cecf1bad8d30fbc841bca16cdfad8681f404d996c989a13`  
		Last Modified: Tue, 13 Aug 2024 01:11:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f419e75d639835961db455968874c2609154a8718db49c30bd01bcd3f203ceb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9495f0e9d8d5d908cf09645d947903f1c147b9bd6e507f6d403b8a9d26aaf15`

```dockerfile
```

-	Layers:
	-	`sha256:5942c214cb7db989d378075c0d9aee72237d12547b77e619b0d50a2298bbbcdd`  
		Last Modified: Tue, 13 Aug 2024 01:11:23 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46577c69618b9a4b72a6a04361191740bff5e460d29af3e9ec4eca8fbde213d`  
		Last Modified: Tue, 13 Aug 2024 01:11:23 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b9fd57e96a4542823ea0d716908b51f6bba602a9d8453f928188bca04332dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266783351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337deb4e17cf6f872fdd2ea35f0e4421d2efd942245565fd2fb584c5f2ef97b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
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
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a020537ba0aca22207306bfa726a5d222fc702ecbd528bb098038498cfe90d`  
		Last Modified: Thu, 25 Jul 2024 19:31:27 GMT  
		Size: 144.0 MB (143959483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19f7860e18fac8ff23741b6fc1e107b8026151279af82e8b32461e806e951c`  
		Last Modified: Wed, 07 Aug 2024 20:08:49 GMT  
		Size: 69.1 MB (69092836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2644aca241993ea8a0965a2799ba74be22026eca543f64520a2595c355879f87`  
		Last Modified: Wed, 07 Aug 2024 20:08:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429275685fccec1f6268f9d5853fb11ff6fe8f7beb9d1223064a26c3bbc0081f`  
		Last Modified: Wed, 07 Aug 2024 20:08:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc043160be94f4b3d630b8c878ebd632b4dd22a5058014a1d9503c9c80517c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae76f6d6dddb7442c73269e789b3538ae94a69c6abba2636c1d2ccb8431a1cf`

```dockerfile
```

-	Layers:
	-	`sha256:dcedfac1fef68f9bee38d47dd25374e7fbe29ca82f8cb6a6bbb066e3077dd846`  
		Last Modified: Wed, 07 Aug 2024 20:08:47 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44bfa628c8c2e119ccb60ccc339bd44735b5d8f8857e6dbaf77f647f5deffbe3`  
		Last Modified: Wed, 07 Aug 2024 20:08:46 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
