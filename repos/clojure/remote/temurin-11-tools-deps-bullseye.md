## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:70063fd72867ebfcf91358112a5de9e94ae63fe9bdb8f2020a47a62799908300
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f0cdc018d262166267b7ff5f0da52573f5f09497d1e96731b0b038fb68878a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269597715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06043607ce3d94994d664cbde5b3275a10c77633454aeaf34297fe180e2ebdf8`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476de739714b2cc9a9887e4f48536128561de906fae111b7f75994829fbb73ad`  
		Last Modified: Sat, 17 Aug 2024 01:59:48 GMT  
		Size: 145.6 MB (145550049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b64567eacb525635ccb11e1aa7d36e579ea6c4dae44cfcf08982f8bdb7d39`  
		Last Modified: Sat, 17 Aug 2024 01:59:47 GMT  
		Size: 69.0 MB (68962344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c863ae01a9c1183bcec670f958cc4f2b3c5d8bbb0c239777f3f14198b1aede4`  
		Last Modified: Sat, 17 Aug 2024 01:59:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4bf49df4e6a765ab5026c46c19feb399fe979c37ae7bc8d8e2e4bd0c4eeafefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7054209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be4a9fae135b5b5c457a0903790a2536a1f90fe0de168f63445b8c6b597e5db`

```dockerfile
```

-	Layers:
	-	`sha256:364f8c80b677d0f104ad220e2192475a99e3c71770c755fb64925823a258b635`  
		Last Modified: Sat, 17 Aug 2024 01:59:45 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc88923eb14d1df3f793ff3cd68e6b43d4fa558e60d642f39acf79df3ae1935`  
		Last Modified: Sat, 17 Aug 2024 01:59:44 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c15b5bad177ebbbb8c3f094fbe4cc5bdd79112f1a83fefe1a726bbe3ecd45f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265180189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07cc49c3b8de4e5505adde42709956d7e8a803227328b0a13c5e3b17bbece2f`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf89200416383f783b253b2a5fd4e6dfd724d574fd700b053360b3ea813e5c1`  
		Last Modified: Tue, 13 Aug 2024 06:24:39 GMT  
		Size: 142.4 MB (142356363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae577614a23aec8551f403fcee12b2109d08c131579fc9f3cbd15262330b4fa`  
		Last Modified: Tue, 13 Aug 2024 06:28:49 GMT  
		Size: 69.1 MB (69093258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98a52e1f4f86bdf2e403a8b51160d551bf2e2be27ee8b850f7886a62ed3630b`  
		Last Modified: Tue, 13 Aug 2024 06:28:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9e144061c7f501ecf4e1db968f664bbf5370d8d2febbdaff80bc0ea120c19627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7060467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddae95b7b30c3bbe0c6671e9fbeca3f83a9943953b65e889ef3602b57dfeff7`

```dockerfile
```

-	Layers:
	-	`sha256:93339c746f0bf60814017da3b5ed72d90356f1d8959545cb4396cf724a7072d9`  
		Last Modified: Tue, 13 Aug 2024 06:28:47 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a309bfd798734deab978e0e57efaa5557172e929eeba03793a3cc2982cb71fe`  
		Last Modified: Tue, 13 Aug 2024 06:28:47 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
