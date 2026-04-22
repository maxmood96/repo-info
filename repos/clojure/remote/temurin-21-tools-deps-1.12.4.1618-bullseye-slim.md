## `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:f4823318c978c341b2015d23e44988f133a4d7ba27a81d3fb033d4f55dfe78c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1fd8bd16616e8bbe2b7864662db4aa5ab0b873a41fca58b1f76d2cf7bf884083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247302575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f924f4078afc237fe7c966e98af37ba49b4c947b11c5856e576e404566c5d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:19:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:59 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a508e71ec02e7a220660db00e74bc645ae2355d0ffcb1fdf41c1501c082fd0`  
		Last Modified: Wed, 22 Apr 2026 02:20:36 GMT  
		Size: 157.9 MB (157857104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b005290d5eeb19ef32d42f7ae5d50fd86f864aa4320a3ce5fe9e51123dfe4a`  
		Last Modified: Wed, 22 Apr 2026 02:20:34 GMT  
		Size: 59.2 MB (59186497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8add59255586f714b72c82e19c0ca6e6da60ce017bd5e705121f62d65a93dc57`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5182ff007a5e444bb20f5af9cbbb133a9eebdf5b1148118b5fe794c138a67c40`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a72b9fb6a9dca192626fbca8258d9c4e41149e9152cc72d114c3c32a79b2b5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1070746e80a0dbf38dc2c174a069fedc0ec624ceeff28e7598f0d8955f8097`

```dockerfile
```

-	Layers:
	-	`sha256:acb64e1fd34db826f9e42acb67732956b8f92c0ec4e56afad0fcfd0ebf25d2d9`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 5.3 MB (5321905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5920d7abd0d58e146e81def3797d9827ccecceb98c9105a16fbf484008abb8`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:06d6d9f44a7791f5f9e46f4c604b530fcaad6f592b08d7487af0eb6bffb81459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244207714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8d59e901af27d0232fcc934611d70ad2505bdc1403e6d4ca87597c763e31b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:22:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:55 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:23:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:23:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3903b6435013c6df9ac7fd65d3f4f76e4ea618ecc0e9d18657ece81297b8b311`  
		Last Modified: Wed, 22 Apr 2026 02:23:33 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d052022098272963f775b30e7c244a96bb46efde0b4ec0d0bcaa65a4be53604`  
		Last Modified: Wed, 22 Apr 2026 02:23:29 GMT  
		Size: 59.3 MB (59331117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0ca895d9b42919223a462186ee1de0d706c9a51f94cd217511f438cb84b886`  
		Last Modified: Wed, 22 Apr 2026 02:23:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc17fc7a3b077325ac0e90e4383b0911453cf50df97052fc95c85e1152d9a4`  
		Last Modified: Wed, 22 Apr 2026 02:23:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff15f59fad2d17bf9c6b3d74566abc83289f80def2dfa074c0c2133a46650e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a496893cfcf85cc040397483187b18a51b3784de3104456c3f6250902a9cde02`

```dockerfile
```

-	Layers:
	-	`sha256:5cb3ffbb884581efcf64bf690f99c0abb78366e85fed0d2addca471f2a131742`  
		Last Modified: Wed, 22 Apr 2026 02:23:27 GMT  
		Size: 5.3 MB (5327637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1316a25a661ab98fe07ba419947d0655a789b244357daea384ab0b7070f5f9a7`  
		Last Modified: Wed, 22 Apr 2026 02:23:27 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
