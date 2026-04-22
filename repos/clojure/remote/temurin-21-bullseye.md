## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:3b7ddfb1891b22aad980262b78c0fe757f335f9532ea43372f307bc853fc7801
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:80b6da630c4a9527f3670bc3cd72cf585459a5377eb4f7aceb923969a0205af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281218716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65eab06ceca7e0b141a351fe1100247d6472813bfdda365d060bfb0202230330`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:19:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:50 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34c323c49eea6e520615009d1273e4f75fd7212ee7480747195963b25f43736`  
		Last Modified: Wed, 22 Apr 2026 02:20:26 GMT  
		Size: 157.9 MB (157857105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09e952ae7071ea027825de4260e67c0ed3ce3a8941380840371dfae92abc097`  
		Last Modified: Wed, 22 Apr 2026 02:20:25 GMT  
		Size: 69.6 MB (69597417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f044e816b7cd5b9083840de9c3d7aaf93008f45c3f61e56513a81af95bbe110`  
		Last Modified: Wed, 22 Apr 2026 02:20:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a5a55a081694f4faf89eaca429e6fc1df3af075e09242d4aba177efca6ce38`  
		Last Modified: Wed, 22 Apr 2026 02:20:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:38aca49a0b84443d030b0ea1ccfbf0e396a4954dce7d7e09750fd56a7d24c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e02d793ee167e0cd7c710ec4157c29712443e715281628a97632588356b17e`

```dockerfile
```

-	Layers:
	-	`sha256:2d6396b9266069493acceb391fd92c9d445f4ee5d56ad5719b35fb8118eebab4`  
		Last Modified: Wed, 22 Apr 2026 02:20:22 GMT  
		Size: 7.4 MB (7409505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1f37d24c8b199fc0225612f2ad6abb3f2289f5732b00f1f9316bff1188f78ae`  
		Last Modified: Wed, 22 Apr 2026 02:20:21 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f29bc61b04705112282e7ae77faa05028fb3d20769110963a6123ea1df2581d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278125756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf87848b9bab6bf57e7ef23a860d8a6a13c06d37fe999f86fa98f40e2f47e08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:22:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:56 GMT
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
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3903b6435013c6df9ac7fd65d3f4f76e4ea618ecc0e9d18657ece81297b8b311`  
		Last Modified: Wed, 22 Apr 2026 02:23:33 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed52a1b10ba6167b2d30061be6250d46c7373308d8b7087e0f456c3ec5254506`  
		Last Modified: Wed, 22 Apr 2026 02:23:32 GMT  
		Size: 69.7 MB (69738670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0ca895d9b42919223a462186ee1de0d706c9a51f94cd217511f438cb84b886`  
		Last Modified: Wed, 22 Apr 2026 02:23:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc17fc7a3b077325ac0e90e4383b0911453cf50df97052fc95c85e1152d9a4`  
		Last Modified: Wed, 22 Apr 2026 02:23:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2c80623c5d8e9f51c93113513d83c7089dd01a8dbbe2371b548bd6af9cdfe284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3981648c660dc4b5442ea8a078497b4193ca36f1f377b75a4748ace054773686`

```dockerfile
```

-	Layers:
	-	`sha256:d49eaecbac76c8c3472402fc5153000f19ae55a46eb051e26aa2f2038fa120be`  
		Last Modified: Wed, 22 Apr 2026 02:23:29 GMT  
		Size: 7.4 MB (7414604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b7258ba60a11ad704346e0a8a519f3513b081f91afda48db022ced4d2ee17c`  
		Last Modified: Wed, 22 Apr 2026 02:23:28 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
