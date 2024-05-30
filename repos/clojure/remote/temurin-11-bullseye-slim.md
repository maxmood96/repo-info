## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:f46cbca5c3986fa8b9a98e87127100ac4d8d1379c48f6ad6045d499abc92eafb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:667d05f198e0bf1842f9059d990307e42a484af20829db6b8c63a3f7c717b1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235359570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f268536191125462f8ac35bb75be00f6b73f7954cbc3059f5413359cf4c37a1c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a35acecdf60bf898a7380a506b15f5e19be888f621c7dbd54348155e3935e00`  
		Last Modified: Wed, 29 May 2024 19:57:08 GMT  
		Size: 145.5 MB (145504874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f7ff7f379b4c794515e1050b17572b4f329b130505bb4ff356f630dd5f7ad3`  
		Last Modified: Wed, 29 May 2024 19:57:07 GMT  
		Size: 58.4 MB (58420116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46705aa55305f5a195e51b3558200105aa38c685a79443d5644c8ed18bac5f66`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81fbe61d5b5de3b9d215959940b5ed55d52f20cc952e5b5e816c39ded63a81de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4923122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289b327081815716c82db5e8b36c208d89f679daba16db6b1aef8fdedc71a9e4`

```dockerfile
```

-	Layers:
	-	`sha256:7d503ca1c6fc1db7aed18ecf872d0218f10683630fbb712274f6bb90d83ca6ee`  
		Last Modified: Wed, 29 May 2024 19:57:06 GMT  
		Size: 4.9 MB (4909234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc24242327c56b0629e73e49a585b436db502f4f9abc1c0abb32fe25be6c2618`  
		Last Modified: Wed, 29 May 2024 19:57:06 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:613ad97e5da1de1e4abbbb98e60d6ee1a74752f17602333f061d84af4f88687d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230931816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065fee02bfd8628e342b213d9b6fd5650003be37257255e81e8220f12ed266f0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c65d67dde4128718a343ddd96ca8084f61812e9a2fd2f2c143f0dc6bbbba9`  
		Last Modified: Wed, 29 May 2024 20:38:19 GMT  
		Size: 142.3 MB (142304134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123e0979a17bf7eefa78d617bf213c1be074a4559129fbbb9b98f9bcfc9dead2`  
		Last Modified: Wed, 29 May 2024 21:23:58 GMT  
		Size: 58.5 MB (58540125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e282fcf4e423927978b0ea8e4152a53e0f119bd8ba37770c3995e8d678b992`  
		Last Modified: Wed, 29 May 2024 21:23:56 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e17eac3ac8ffe915d5f810bfed0e11fbcb8eba15f2238a35cd1c9a047645d4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b108076d6cbd80be48a724919a43653e821abec8a6658af203562d210b4d2920`

```dockerfile
```

-	Layers:
	-	`sha256:80736fb3b964c3370b0ad7dbd0c5881b90acab77e8802f7b1f471fe2ffbb628b`  
		Last Modified: Wed, 29 May 2024 21:23:57 GMT  
		Size: 4.9 MB (4915590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed54c5ddfe48e155cc669d77ef9b5d6c4c23ccc9bd239bc653d3871fd354b4f`  
		Last Modified: Wed, 29 May 2024 21:23:56 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json
