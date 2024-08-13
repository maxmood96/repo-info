## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:4fa7f2aea485eee97924b012b11d5958640a47ed8cdfe3839b466131b3092e07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dafa2a338358f7777a1fb55dc9e413528611e8880984fd3a9afd373ef14b3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256730522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c36653b7993848931c49963d043c00088c4fb6983eb80e86761e06c4a0d18`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ff9c6c401ce016dc8f229ff95eba7f99c4daf9e2bce87884367230a0ceb951`  
		Last Modified: Tue, 13 Aug 2024 01:11:29 GMT  
		Size: 158.6 MB (158579315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41dfa9990968df8379ac65c9723d9527b1bfad27ca02eb3eae3f2da7542a8d6`  
		Last Modified: Tue, 13 Aug 2024 01:11:28 GMT  
		Size: 69.0 MB (69023936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687f481a174f50fda0b4c5933770d8fab77c4c4bb1d4af4558a98c33e057bfb6`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4b72f849b94d316a5a6ad878f5e2241a7c80377ffb219b6749b9f262b11dd`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6adaadc941af915f98507b644cdfd515e34c903b39ddf445d4ac685a2c6c5718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4762079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132cbd94ecfbbecfc91aef44174e6a07b8857c83bf83ab067115698ecb7048d0`

```dockerfile
```

-	Layers:
	-	`sha256:5dcc8fdef87841a2e483733bb24084f773ec63ba5ffd312d7a3e772686f40e32`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 4.7 MB (4745870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc6d52f483e15739db18c0eeb1acb159a470ce46790319b582160718f9c6b1d5`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08c57d5c539b42c460c6cd5e3c20af05fb881f8b15fc7fcd8c18aa304339ab7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254677341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b41acef14298709d52bc507d577b38d6b9e5abce9224e7a65152a2126d13dc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc886ce209c192998c2b3f4ed4247246a0d7842bf3146abd8f602bc2fac044b9`  
		Last Modified: Thu, 25 Jul 2024 19:40:41 GMT  
		Size: 156.7 MB (156746213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d838264c105dd721db7bd05ae09078acc3368933367072653ad24e7b9336ae`  
		Last Modified: Wed, 07 Aug 2024 20:12:54 GMT  
		Size: 68.8 MB (68773512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3543f62f8ce2b3d086014502363d2e3a13c5569913108a406063b47839f3a4e2`  
		Last Modified: Wed, 07 Aug 2024 20:12:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fff337e8b64b8838b9117baeca3ed55d7338c1d0730fd178d5c125c626ad3d8`  
		Last Modified: Wed, 07 Aug 2024 20:12:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d7dd0db4f67a5fb14b4d72fe9ed060ddfe7358d3448268120ca9be85de8e4c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4769052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7295df53bdb9b2dfcea5001309cf05b9dc1196ccac939b995969cd41cc5606c`

```dockerfile
```

-	Layers:
	-	`sha256:933c933ea9f7512af680553b0089ef690a6c2919fd98121f811c172ba1a558d7`  
		Last Modified: Wed, 07 Aug 2024 20:12:53 GMT  
		Size: 4.8 MB (4752279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9110205e7d0577c878da7e3ff8c518e574832df8e53b5f5c55ce7587dce7f6`  
		Last Modified: Wed, 07 Aug 2024 20:12:52 GMT  
		Size: 16.8 KB (16773 bytes)  
		MIME: application/vnd.in-toto+json
