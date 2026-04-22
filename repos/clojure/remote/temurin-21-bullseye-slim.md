## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:6ceb26aee76b469bffe2e0f58abd327c00afdd116b657455c4cdc939705f5a1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e1c78b11de0d1a8ba4cd496d4b6d9a2e73f1ea4d14b2dede32b97b1513d989ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247308106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf8b98209bc5fa39dd880c572e4a7a401aa34f734a87a9316ffefaf9922d5a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:05:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:34 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7630267f7564171bdcaf989c60bc746580da069489e9945be7b3136434a761`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 157.9 MB (157857060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cffe32cbcde9a6777125dccc8385773f5b919b0dfa9c3c6e7e02ec9eca1346`  
		Last Modified: Wed, 15 Apr 2026 22:06:11 GMT  
		Size: 59.2 MB (59191984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f989607a3b35a02b82791e15794d7f4bbce1384facc535535e76f553e2b890e`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46c78bf30db179be7bca6702610f41c0c699ffa60d97405a07d44b0d67756cb`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52c42fe92bf8fc8f06b0f9e66e66f87b259f639058e0057ce1e388e500474144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96d8aa75ae900f59a52ef14b5183e747384d99cd7e26403d897bda9919eae92`

```dockerfile
```

-	Layers:
	-	`sha256:e287cee5e5a44591eedd046f4bf68bcd657dc1ba504908ad4e8e240efe98a7a0`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 5.3 MB (5321905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744c2c76ee7e85cba08350e425a1bc697a04a83152c26c4c977a5c4e7ca69884`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

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
